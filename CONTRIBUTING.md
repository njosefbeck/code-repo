# Contributions
How do you go about submitting code examples? Read below to find out!

## Steps to take:
1. [Fork](https://guides.github.com/activities/forking/) the repository and clone it locally. Connect your local to the original ‘upstream’ repository by adding it as a remote. Pull in changes from ‘upstream’ often so that you stay up to date so that when you submit your pull request, merge conflicts will be less likely. See more detailed instructions [here](https://help.github.com/articles/syncing-a-fork/).

2. Create a [branch](https://guides.github.com/introduction/flow/) for your edits.

3. Once you’ve opened a pull request a discussion will start around your proposed changes. Other contributors and users may chime in, but ultimately the decision is made by the maintainer(s). You may be asked to make some changes to your pull request, if so, add more commits to your branch and push them – they’ll automatically go into the existing pull request.


## Format for Contributions
Please follow these guidelines when you write up your code examples.

For each example, use Markdown to format your entry and include the fields shown in the example below. First you'll see the example and then the Markdown code used to format the example.

### Example 1
* **LANGUAGE:** CSS3
* **TOPICS:** Media Queries, Classes, Display
* **SOURCE:** Mozilla Developer Network
* **URL (if applicable):** [https://developer.mozilla.org/en-US/docs/Web/Guide/CSS/Media_queries](https://developer.mozilla.org/en-US/docs/Web/Guide/CSS/Media_queries)

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

**MARKDOWN FOR THIS EXAMPLE**

```markdown
### Example 1
* **LANGUAGE:** CSS3
* **TOPICS:** Media Queries, Classes, Display
* **SOURCE: (if applicable)** Mozilla Developer Network
* **URL:** [https://developer.mozilla.org/en-US/docs/Web/Guide/CSS/Media_queries](https://developer.mozilla.org/en-US/docs/Web/Guide/CSS/Media_queries)

**Code:**
```css
@media (max-width: 600px) {
 	.facet_sidebar {
		display: none;
     }
}

**Explanation:**
This media query targets screen widths of 600px or less, hiding the element with class .facet-sidebar by changing its display to 	none. So, that element will not appear on the screen in resolutions of 600px or less.
```

