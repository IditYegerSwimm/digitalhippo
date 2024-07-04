---
title: The CartItem component
---
This doc will describe cart item component that will be used in&nbsp;&nbsp;

<SwmSnippet path="/src/components/CartItem.tsx" line="8">

---

This is a component that renders a single item in the cart and displays the product's image, category and a button to remove the item from the cart

```tsx
const CartItem = ({ product }: { product: Product }) => {
  const { image } = product.images[0]

  const { removeItem } = useCart()

  const label = PRODUCT_CATEGORIES.find(
    ({ value }) => value === product.category
  )?.label
```

---

</SwmSnippet>

## The <SwmToken path="/src/config/index.ts" pos="1:4:4" line-data="export const PRODUCT_CATEGORIES = [">`PRODUCT_CATEGORIES`</SwmToken> dictionary

&nbsp;The <SwmToken path="/src/config/index.ts" pos="1:4:4" line-data="export const PRODUCT_CATEGORIES = [">`PRODUCT_CATEGORIES`</SwmToken> dictionary contains the labels for each product category, for example, the&nbsp;

<SwmMeta version="3.0.0" repo-id="Z2l0aHViJTNBJTNBZGlnaXRhbGhpcHBvJTNBJTNBSWRpdFllZ2VyU3dpbW0=" repo-name="digitalhippo"><sup>Powered by [Swimm](https://staging.swimm.cloud/)</sup></SwmMeta>
