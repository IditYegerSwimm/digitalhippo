---
title: The CartItem component
---
This doc will describe cart item component that will be used in&nbsp;&nbsp;

<SwmSnippet path="/src/components/CartItem.tsx" line="8">

---

This is a component that renders a single item in the cart and displays the product's image, category and a button to remove the item from the cart

&nbsp;const { label } = <SwmToken path="/src/components/CartItem.tsx" pos="11:11:13" line-data="  const { removeItem } = useCart()">`useCart()`</SwmToken> get the label from the `PRODUCT_CATEGORIES` arrayget the label from the `PRODUCT_CATEGORIES` arrayuse the `label` variable to get the label from the `PRODUCT_CATEGORIES` array

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

## The <SwmToken path="/src/config/index.ts" pos="1:4:4" line-data="export const PRODUCT_CATEGORIES = [">`PRODUCT_CATEGORIES`</SwmToken> dictionary  contains the labels for each product categoryand their corresponding values

&nbsp;The <SwmToken path="/src/config/index.ts" pos="1:4:4" line-data="export const PRODUCT_CATEGORIES = [">`PRODUCT_CATEGORIES`</SwmToken> dictionary also contains the labels for each product category, for example, the UI_Kits is&nbsp;

## The <SwmToken path="/src/hooks/use-cart.ts" pos="15:1:1" line-data="  removeItem: (productId: string) =&gt; void">`removeItem`</SwmToken> function is used to remove the item from the cart

<SwmMeta version="3.0.0" repo-id="Z2l0aHViJTNBJTNBZGlnaXRhbGhpcHBvJTNBJTNBSWRpdFllZ2VyU3dpbW0=" repo-name="digitalhippo"><sup>Powered by [Swimm](https://staging.swimm.cloud/)</sup></SwmMeta>
