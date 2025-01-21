

### Summary:

- **`min-height`** = Apply styles to **larger screens** (height >= value).
- **`max-height`** = Apply styles to **smaller screens** (height <= value).
- 

`min-height` - applies to the styles if the height of the devices or viewport is atleast the specifified value( it's like the minimum)

```css
@media (min-height: 600px) {
  body {
    background-color: blue;
  }
}

```

**Effect**: The background will turn blue if the height is **600px or more**

`max-height`

**Definition**: Applies the styles if the height of the device or viewport is **at most** the specified value.

```css
@media (max-height: 600px) {
  body {
    background-color: green;
  }
}

```