# Accessibility at Truss

This is the primary repository of information and resources surrounding accessibility practices at Truss.

## Tracking work

Issues and their progress will be captured on the [Github project board](https://github.com/trussworks/accessibility/projects/1).

## Guild

Discussion and support at [#g-accessibility](https://trussworks.slack.com/app_redirect?channel=g-accessibility)

## Guide

### What is accessibility?

Accessibility (also abbreviated as a11y) is making sure that a greater number of users are able to access and use your product.

### Accessibility is inclusion

Accessibility is not just making sure that a web application is usable by those with physical limitations. While it is very important for those that rely on screen readers and other assistive devices to be able to use the application, other limiting factors can include: type of device, language, content, bandwidth, etc. Ideally we wish to include as many different types of users and situations to be able to access our application as realistically as we can.

### Government compliance

All federal web applications have accessibility requirements (typically written into contracts) which may also apply at the state and city level. Common thresholds for compliance include 508 and WCAG 2.1 AA.

### Commercial compliance

While not commonly required, we should also be aware of why accessibility can be important for commercial applications as well. Commercial applications may be subject to legal, legislative, reputation, and/or ethical reasons to follow accessibility guidelines.

### Accessibility is important during the entire project lifecycle

Accessibility needs to be incorporated throughout the entire lifecycle of a project, it should not be incorporated as an afterthought or checked only towards the end. It is much easier to address issues during feature conception, development, and story creation phases; as a consequence, it will save time and therefore become more cost effective for the project.

### Accessibility is important across practices

Every role in the project should be aware of the importance of accessibility and have a basic understanding of how they are addressed (even if they only know to look at this guide as a reference first). Accessibility should not be beholden to only one practice to address (e.g. just engineers to fix tags or designers to figure out color and content), but it should be the shared responsibility of everyone on the project. An effective team can work together to make sure that accessibility concerns are met throughout the entire project lifecycle.


### Resources

- [Intro to Accessibility OTT, Dec 2019](https://docs.google.com/presentation/d/1Itmkkj2OHX2JuA58aFR7Uj77EDw9Wz0Mt5EgLivK_a4/) 🔒
- [18F Accessibility Guide](https://accessibility.18f.gov)
- [Accessibility for teams](https://accessibility.digital.gov/)
- [Mozilla Accessibility Learn Web Development Documentation](https://developer.mozilla.org/en-US/docs/Learn/Accessibility)
- [7 things every designer needs to know about accessibility](https://medium.com/salesforce-ux/7-things-every-designer-needs-to-know-about-accessibility-64f105f0881b)
- [Designing for Accessibility and Inclusion](https://www.smashingmagazine.com/2018/04/designing-accessibility-inclusion/)
- [VOX accessibility guidelines](http://accessibility.voxmedia.com/)
- [plainlanguage.gov](https://www.plainlanguage.gov/)

## Guidance based on role

### Design/content
The following sections outline aspects of accessibility to keep in mind during the research and design process.

**Forms/controls**

Focus states should easily indicate what control or form element is active

- When people use the keyboard to navigate, your product should properly indicate which element they are selecting using highly visible focus states.
A good focus indicator doesn’t rely on color alone, think of ways to indicate focus using a combination of color, size, pattern, ect. (for example, try applying the same styling you give to elements on hover plus an outline)

Forms should have visible boundaries and labels

- Clearly defined boundaries for form fields are important for users with mobility issues. These boundaries help define the location and size of a click target.
- Labels tell the user the purpose of the field and should maintain that use as people interact with form fields.
- Placeholder text should not be a replacement for a visual label.

Form submission should trigger a meaningful message

- Explicit context change should happen after a form is submitted. Such as, showing a static success message and shifting focus to it upon its appearance.

Users should be able to accurately select a control

- The recommended minimum size of controls is 44x44px. This size also includes any padding the control has.
- Controls should also be spaced far enough apart to reduce touch errors. A minimum of 8px is recommended.

Error messages should be visible and specific

- Use multiple cues like color, icons, bold font weight, heavy border or outline, and helpful text to make sure users don’t overlook this critical information.
- A common mistake is relying solely on the user of “red” to communicate error states.


**Layout**

Visual layout and structural (HTML) layout should match

- Screen readers use the structural layout to help users navigate through a product. When the visual layout changes but not the structural layout, screen readers can become confused and break tab order.
- If you need to change the visual layout also change the underlying structural layout.

Layouts should be scalable

- Layouts should be flexible enough to allow users to zoom up to 400% without breaking the layout causing navigation and readability issues.

### Engineering

**Semantic HTML**

- Use the correct HTML for an element
- Make sure the correct ARIA tags are used
- HTML document has language set
- Tables are laid out properly
- Headings nested properly

**Keyboard Navigation**
- The application should be keyboard accessible
- The application should be free from keyboard traps, so a - user cannot be stuck in a loop
- Ability to skip navigation to access main content
- Make sure the application never loses focus, it should always be visible while navigating the page.
- Tab order should be logical, so that navigation makes sense

**Links, text, and descriptions**

- Make sure links are descriptive and not vague (i.e. “link” or “here” is not useful)
- Links should be easily identifiable with defined `:focus` and `:active` states
- Text should have sufficient color contrast
- Page titles are descriptive

**Forms**

- Labels should always be present to identify each form element
- Instructions for input elements are clear
- All field elements should be accessible by keyboard
- Descriptive error messages that are not only defined by color
- Test how ARIA affects form inputs

### Product

- Product should advocate for accessibility as the way we work from the beginning and not a line item to add at the end
- Product should understand the work as done by other groups
- Product should prioritized accessibility needs on the roadmap
- Product should hold space for iteration when needed on accessibility


### Useful tools
- [AXE browser extension](https://www.deque.com/axe/) - in browser accessibility testing
- [A11y storybook add-on](https://github.com/storybookjs/storybook/tree/next/addons/a11y) - React accessibility testing in Storybook
- [Chrome Lighthouse (accessibility report)](https://developers.google.com/web/tools/lighthouse) - Accessibility audit in Chrome DevTools
- [HTML_CodeSniffer (browser bookmarklet)](https://squizlabs.github.io/HTML_CodeSniffer/) - Accessibility Auditor Bookmarket
- [Color contrast checker](https://webaim.org/resources/contrastchecker/) - Interactive online color contrast checker for foreground and background ratios
- [How to allow full keyboard navigation in Mac OS browsers](https://www.a11yproject.com/posts/2017-12-29-macos-browser-keyboard-navigation/) - By default, Apple computers have an operating system (OS) level setting that limits the Tab key to "Text boxes and lists only". This guide shows how to change it.

------

## VoiceOver guide

### How-to use the rotor menu
- Turn voice over on cmd + F5
- Open rotor menu ctrl + option + U (you’ll see a panel appear)
- Use ⬅️ and ➡️ to cycle through the rotor menu
- Use ⬆️ and ⬇️ to move down that rotor view
- When you are done you can dismiss the rotor menu by hitting Esc
- Turn voice over off cmd + F5

[Video demo for the rotor menu](https://trussworks.slack.com/archives/C01BCRE1Q20/p1620842498214400)

