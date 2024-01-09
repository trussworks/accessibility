# Design and a11y review process

Per our [design review DR](adr_design-review.md), The below steps are specifically the design and accessibility testing part of the overall acceptance flow process. The code submitter should have done their due dilligence for any user interface changes so that a design/a11y reviewer can focus on finer details. Although there are several steps, if we do this regularly it will be a light lift and will avoid any design/a11y debt.

## Get ready

1. Consider conducting this with your engineer, who can help diagnose and articulate problems and solutions to what you may find in this process.
2. Load the [frontend application](https://truss.works) (this updates on every merge to the [main](https://github.com/trussworks/accessibility/main) branch)
3. Open the PR(s) with the https://github.com/trussworks/accessibility/labels/needs%20design%20review label to review.
4. Use the checklist in the next section to review the changes, noting what the original developer checked off in their "user-facing" checklist
5. For each PR you review, remove the https://github.com/trussworks/accessibility/labels/needs%20design%20review label
6. Create a [new issue](https://github.com/trussworks/accessibility/issues/new/choose) with the "Bug" template, and document a problem you find, linking to the relevant PR and `@`ing the original developer for context (don't "assign" unless they're ok with it).
   * Repeat this step for each issue you find. To help engineers portion and pace work, it's usually best to not bundle everything into a single issue. Instead, use one issue for each discrepancy or highly related group of discrepancies.

## Verify that any changes match the design intention

- [ ] Check that the design translated visually
- [ ] Check interaction behavior
- [ ] Check different states (empty, one, some, error)
- [ ] Check for landmarks, page heading structure, and links
- [ ] Try to break the intended flow
- [ ] Confirm this works at 5Mbps down and 1Mbps up. You might use [Firefox dev tools](https://firefox-source-docs.mozilla.org/devtools-user/network_monitor/throttling/index.html) or Chrome's [WebRTC Network Limiter](https://chrome.google.com/webstore/detail/webrtc-network-limiter/npeicpdbkakmehahjeeohfdhnlpdklia)

## Verify that any changes meet accessibility targets

- [ ] Check responsiveness in mobile, tablet, and desktop at 200% zoom
- [ ] Check keyboard navigability

* Test general usability, landmarks, page header structure, and links with a screen reader (different from what the original dev used in their checklist):
  - [ ] [VoiceOver](https://dequeuniversity.com/screenreaders/voiceover-keyboard-shortcuts#vo-mac-basics) in Safari
  - [ ] [JAWS](https://dequeuniversity.com/screenreaders/jaws-keyboard-shortcuts#jaws-the_basics) in Chrome
  - [ ] [NVDA](https://dequeuniversity.com/screenreaders/nvda-keyboard-shortcuts#nvda-the_basics) in Chrome
* Use an a11y tool to check these changes conform to at least WCAG 2.1 AA
  - [ ] [WAVE](https://wave.webaim.org/)
  - [ ] [axe](https://www.deque.com/axe/devtools/)
  - [ ] [ANDI](https://www.ssa.gov/accessibility/andi/help/install.html#install)
  - [ ] Browser inspector ([firefox](https://firefox-source-docs.mozilla.org/devtools-user/accessibility_inspector/#accessing-the-accessibility-inspector) / [chrome](https://developer.chrome.com/docs/lighthouse/accessibility/))
  - [ ] For storybook-only components, use its [accessibility addon](https://medium.com/storybookjs/instant-accessibility-qa-linting-in-storybook-4a474b0f5347#c703).