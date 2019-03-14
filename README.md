# High Contrast Mode Reduced Test Cases

Last Updated: 2019-03-14

## Overview
The following is a collection of test cases comparing different styling of inputs when High Contrast Mode is enabled.

High contrast is a Windows accessibility feature intended to increase the readability of text through color contrast. Individuals with low vision may find it more comfortable to read content when there is a strong contrast between foreground and background colors. High contrast is a useful feature in increasing the readability of screen-based text for such users.

The Windows platform provides built-in high contrast color themes such as the more popular "black-on-white" and "white-on-black" themes. Besides the default themes, users can customize the colors and create their own themes. Applications can make use of these color themes and propagate them into their content model. In the case of the web browser, high contrast colors are propagated to website pages as a set of user agent styles, thus increasing readability of the text and allowing a coherent experience across the Windows OS and various applications. — [Ref. 1](#References)

Internet Explorer and Edge have a vendor-prefixed `-ms-high-contrast` media feature which allows developers to detect if the user is currently in Windows High Contrast Mode, and to apply specific additional style rules in that situation. — [Ref. 2](#References)

Google Chrome will prompt the user to install the [High Contrast extension](https://chrome.google.com/webstore/detail/high-contrast/djcfdncoelnlbldjfhinnjlhdjlikmph) while Mozilla Firefox supports Windows high contrast mode; Firefox does not support the `-ms-high-contrast` CSS media feature as it is non-standard. — [Ref. 3](#References)

While Windows supports High Contrast Mode, macOS applies an invert color setting which impacts the entire operating system including browsers and the content within them. — [Ref. 4](#References) The inverted color setting allowed users to switch between light-on-dark / dark-on-light text (with the side effects of inverting images for example); this is somewhat similar to how Window's High Contrast mode offers a black-on-white / white-on-black color theme where the side effect on the Window's side being background images being ignored (with the exception of Microsoft Edge — [Ref. 5](#References) which Microsoft Edge applies an intermediary layer behind all text to ensurce contrast lying above images — [Ref. 6](#References))

**User Preference Media Features**
While the CSS Level 5 media query draft has [multiple user preferences](https://drafts.csswg.org/mediaqueries-5/#mf-user-preferences) which covers some of the topics discussed above such as:
 * [inverted-colors](https://drafts.csswg.org/mediaqueries-5/#inverted)
 * [prefers-color-scheme](https://drafts.csswg.org/mediaqueries-5/#prefers-color-scheme) (Note: High contrast mode could be used as a makeshift "nightmode" for those working with applications that don't offer a nightmode/high contrast/dark theme)

For the sake of this repo, the focus will be on True high contrast, which is along the lines of Windows High Contrast Mode, which currently is [prefers-contrast](https://drafts.csswg.org/mediaqueries-5/#prefers-contrast) in the CSS Level 5 media query draft.

> This is intended for users with unusual vision impairments, who may also use other accommodations such as screen magnification to be able to access content.
> * This is often an operating system setting which affects how text, borders and images are displayed. In this case, developers may wish to make adjustments to ensure that these modifications don't create other problems.
>
> — [Ref. 7](#References)

## Tests
**Tests 01 - 14:** While not a true "reduced" test case collection, this shows an example in which someone may need to set the input's background to appear transparent. These test focus on the background shorthand css property `background:`

**Tests 15 - 26:** These test are similar to Test 01 - 14 but uses `background-color` so tests 13 & 14 are not included here.

**Test 27:** This test is an example of Material Design Filled text fields.

**Test 28:** Reduced test case.

### Versions & Environment

**Operating System:** Windows 10 Pro
 - *Version:* 1809
 - *OS build:* 17763.348
 
 **Browsers:**
 - Microsoft Edge 44.17763.1.0, Microsoft EdgeHTML 18.17763
 - Microsoft Internet Explorer 11, Version: 11.379.17763.0, Update Versions: 11.0.115
 - Firefox Quantum, Version: 65.0.2 (64-bit)
 - Firefox ESR, Version: 52.9.2 (64-bit)


### References
1. Microsoft Edge Explainers on the subject of [High Contrast](https://github.com/MicrosoftEdge/MSEdgeExplainers/blob/master/HighContrast/explainer.md)
2. Paciello Group blog post titled [Windows High Contrast Mode: the limited utilitiy of -ms-high-contrast](https://developer.paciellogroup.com/blog/2016/12/windows-high-contrast-mode-the-limited-utility-of-ms-high-contrast/)
3. MDN web docs on [-ms-high-contrast](https://developer.mozilla.org/en-US/docs/Web/CSS/@media/-ms-high-contrast) CSS media feature
4. Adrian Roselli's blog post titled [OS: High Contrast versus Inverted Colors](http://adrianroselli.com/2017/11/os-high-contrast-versus-inverted-colors.html)
5. [Quick Note on high contrast mode](https://www.scottohara.me/blog/2019/02/12/high-contrast-aria-and-images.html#background-images-are-mostly-ignored)
6. Microsoft Edge Explainers - [Ensuring Readability](https://github.com/MicrosoftEdge/MSEdgeExplainers/blob/master/HighContrast/explainer.md#ensuring-readability)
7. CSS Level 5 media query w3c/csswg-draft topic [prefers-contrast: high media feature does not accurately describe the macOS/iOS state](https://github.com/w3c/csswg-drafts/issues/2943#issuecomment-452164677)
