# tailwindcss-tooltips
Very simple css only tooltips for Tailwind css. See the demo at https://jsfiddle.net/xjnw5vdz/1/

# Add in your css file the following:

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

# Use the tooltips like this:

```
<p class='tooltip'>
Hover me <span class='tooltip-text bg-blue-200 p-3 -mt-6 -ml-6 rounded'>Look at this!</span>
</p>
```
or:

```
<div class='tooltip m-10 border border-blue-400 rounded p-10'>
  <p> Hoovering over this div will show the tooltip. You can position tooltips using -m and m like -mt-12 </p>
  <span class="tooltip-text bg-yellow-400 border rounded border-orange-500 text-orange-700 -mt-12">Hey There!</span>
</div>
```
