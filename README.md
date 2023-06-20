# tailwindcss-tooltips
Very simple css only tooltips for Tailwind css. See the demo at https://play.tailwindcss.com/2eBipAu8Bt

# Edit your Tailwind.css file:
Add the followind code on your Tailwind.css file:

```
.tooltip {
  @apply invisible absolute;
}

.has-tooltip:hover .tooltip {
  @apply visible z-50
}

```
In the `.tooltip` class you can add some defult syle like `p-1 rounded border border-gray-200 bg-gray-100 shadow-lg ml-4 text-sm`
It's reccomended to add at least `bg-white` to avoid that the tooltip text shows over the partent text.

If you can't use `@apply` you can add this CSS instead:

```
.tooltip{
  visibility: hidden;
  position: absolute;
}
.has-tooltip:hover .tooltip {
  visibility: visible;
  z-index: 100;
}
```
Also in this case in the `.tooltip` class you can add some default padding, text color, background color, etc  like `background:#fff;`


# Use the tooltips

To use the tooltip simply wrap a `tooltip` element inside a `has-tooltip` element like this:

```
<p class='has-tooltip'>
  Hover me <span class='tooltip'>Look at this!</span>
</p>
```
You can edit the tooltip position & style using Tailwind CSS classes like so:

```
<div class='has-tooltip'>
  <span class='tooltip rounded shadow-lg p-1 bg-gray-100 text-red-500 -mt-8'>Some Nice Tooltip Text</span>
  Custom Position (above)
</div>
```

You can also change the position of the tooltip depending on the device using Tailwind's responsive modifiers

For example: `-mt-1 lg:-mt-8`

```
<p class='has-tooltip'>
<span class='tooltip bg-blue-200 p-3 -mt-1 lg:-mt-8 rounded'>Look at this!</span>
Hover me
</p>
```

## Example:

You can view a specific example at:
- https://play.tailwindcss.com/2eBipAu8Bt (Reccomended way with @apply)
- https://jsfiddle.net/jvb52qh3/ (Alternative way without @apply)
