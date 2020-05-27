# tailwindcss-tooltips
Very simple css only tooltips for Tailwind css. See the demo at https://jsfiddle.net/xjnw5vdz/1/

# Edit your CSS:

Add in your css file the following:

```
.tooltip .tooltip-text {
  visibility: hidden;
  text-align: center;
  padding: 2px 6px;
  position: absolute;
  z-index: 100;
}
.tooltip:hover .tooltip-text {
  visibility: visible;
}
```

If you prefer to use the @apply directive (from Tailwind CSS) you can instead add in your css file:

```
.tooltip .tooltip-text {
  @apply invisible p-4 absolute z-50 inline-block ml-4 text-sm w-1/2 rounded-lg bg-gray-700 text-white;
}

.tooltip:hover .tooltip-text {
  @apply visible;
}

```
# Use the tooltips

To use the tooltip simply wrap a `tooltip-text` element inside a `tooltip` element like this:

```
<p class='tooltip'>
Hover me <span class='tooltip-text bg-blue-200 p-3 -mt-6 -ml-6 rounded'>Look at this!</span>
</p>
```
or:

```
<div class='tooltip m-10 border border-blue-400 rounded p-10'>
  <p> Hovering over this div will show the tooltip. You can position tooltips using -m and m like -mt-12 </p>
  <span class="tooltip-text bg-yellow-400 border rounded border-orange-500 text-orange-700 -mt-12">Hey There!</span>
</div>
```

You can also change the position of the tooltip depending on the device using Tailwind's responsive modifiers

For example: `-mt-1 lg:-mt-8`

```
<p class='tooltip'>
<span class='tooltip-text bg-blue-200 p-3 -mt-1 lg:-mt-8 rounded'>Look at this!</span>
Hover me
</p>
```
