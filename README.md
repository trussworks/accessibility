# Accessibilty at Truss

This is the primary repository of information and resources surrounding accessibility practices at Truss.

## Tracking work

Issues and their progress will be captured on the [Github project board](https://github.com/trussworks/accessibility/projects/1).

## Guild

Discussion and support at #g-accessibility

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

**Color and text**

Don’t use color as the only visual means of conveying information

- There should be another indicator (such as icons, text, or pattern) so that people who cannot easily distinguish colors will be able to understand the content.

**Make sure the foreground and background color of all text, icons, and focus indicators meet the proper contrast ratio**

- The contrast ratio between texts and background should be at least 4.5:1 according to the WCAG.
- If your font size is at least 24px or 19px bold, the minimum decreases to 3:1.

**Don’t use overly saturated or high contrast colors**

- Oversaturated colors, high contrast colors, or even just the shade of the color can be unsettling for users.
- It’s best to avoid high concentrations of these types of colors.

**Typography should be easy to read and scalable**

- Font sizes should be responsive and the design should allow for users to zoom without causing readability issues.
- The font itself should be easy to read. Decorative fonts, small font sizes, italicized text, and all uppercase text are harder to read.
- Larger text, shorter line lengths, taller line heights and increased letter spacing improves readability.

**Images and icons**

Make sure images have proper alt text

- Users that rely on browsers to read content for them rely on alt text to provide meaning to an image.
- It’s recommended to describe all of the elements that explain what’s happening in the image rather than just providing a simple title.
- Descriptions should be succinct, it’s recommended to go no longer than two sentences.
- If the product that you are designing allows users to upload images, you should provide the ability to enter alt text along with the file.
- If an image is purely decorative, an empty alt tag should be included so that the user is not read alt text that doesn’t enhance usability.

**Images and icons should be easily understandable**

- Avoid using graphics when written content could communicate the same thing.
- Use icons as helpful visual cues to connect to concepts. Only use icons purposefully and not for decoration. Use familiar icons that people are accustomed to associating with common actions, like a trash can to represent deleting something.

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

**Animation and effects**

Understand why you are using animation and effects and how to design them safely

- Fast flashing effects (defined as flashing more than three times a second) or high-intensity effects and patterns can cause seizures, known as ‘photosensitive epilepsy.’
- Parallax or motion effects, can cause some users to feel dizzy or experience vertigo due to vestibular sensitivity.
- Constant animations or motion can also be distracting to users, especially to users who have difficulty concentrating
- Provide controls or options to stop, pause, hide, or change the frequency of any animations or effects

**Audio and video**

Avoid autoplaying videos and audio

- Constantly moving animations and video can be distracting. You should provide controls or options to pause or disable the video or audio.

Provide transcripts or subtitles

- Video should have transcripts or subtitles so people can review the material in the best way that suits their needs
- Transcripts should include descriptions, not exclusively dialog/narration. This is particularly important for blink folks, who might make use of the transcript to make sure they didn’t miss anything by only taking in auditory information.

**Layout**

Visual layout and structural (HTML) layout should match

- Screen readers use the structural layout to help users navigate through a product. When the visual layout changes but not the structural layout, screen readers can become confused and break tab order.
- If you need to change the visual layout also change the underlying structural layout.

Layouts should be scalable

- Layouts should be flexible enough to allow users to zoom up to 400% without breaking the layout causing navigation and readability issues.

**Content/readability**

Content should be concise, clear, and well organized

- Content should be written using plain and simple language
- Paragraphs should be focused on a single idea
- Ideal line length should between 45 and 75 characters
- Breaking up content with headings, lists, or images give mental breaks to readers
- Use headings to logically group and summarize information
- Be consistent with placement and labeling
- Interactive components should have meaningful labels (e.g. buttons, menus, links)

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

**Media**

- All images should use an img tag
- Multimedia should be tagged (captions, audio descriptions, etc)
- SVGs should be accessible to assistive devices
- Hide decorative images from assistive devices using an empty alt tag (`alt=""`)

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

**Interactions**

- Avoid timeouts for feature interactions. If you must, then give the option to extend the time.
- Check that any elements that flash on screen do so at a rate of less than 3 Hz

**Styling**
- Ensure that the application still makes sense with CSS turned off.

### Product

- Product should advocate for accessibility as the way we work from the beginning and not a line item to add at the end
- Product should understand the work as done by other groups
- Product should prioritized accessibility needs on the roadmap
- Product should hold space for iteration when needed on accessibility


### Useful tools
- [AXE browser extension](https://www.deque.com/axe/)
- [A11y storybook add-on](https://www.deque.com/axe/)
- [Chrome Lighthouse (accessibility report)](https://www.deque.com/axe/)
- [HTML_CodeSniffer (browser bookmarklet)](https://www.deque.com/axe/)
- [Color contrast checker](https://www.deque.com/axe/)
