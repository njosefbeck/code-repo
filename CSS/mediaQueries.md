# CSS : Media Queries
Below you will find examples of media queries. 

### Example 1
* **Language:** CSS3
* **TOPICS:** Media Queries, Classes, Display
* **SOURCE:** Mozilla Developer Network
* **URL:** [https://developer.mozilla.org/en-US/docs/Web/Guide/CSS/Media_queries](https://developer.mozilla.org/en-US/docs/Web/Guide/CSS/Media_queries)

**Code:**
```css
@media (max-width: 600px) {
 	.facet_sidebar {
		display: none;
     }
}
```
**Explanation:**

This media query targets screen widths of 600px or less, hiding the element with class .facet-sidebar by changing its display to 	none. So, that element will not appear on the screen in resolutions of 600px or less.
