# Audit areas: what to look at and what counts as evidence

Optional depth for step 3 of `SKILL.md`. Pick the areas that match the user's goals; you do not need to cover all of them.

For every area, remember: **Observed** needs a URL and a method. If your tools cannot show something, put it under **Needs testing**.

## Contents
1. Clarity of message
2. Navigation and structure
3. Mobile experience
4. Accessibility
5. Trust signals
6. Calls to action
7. Technical hygiene
8. Evidence quick-reference

## 1. Clarity of message
**Look for:** Can a first-time visitor tell what this is, who it is for, and what to do next, from the top of the home page? Is the headline specific? Is the value proposition stated in plain language?
**Evidence:** Page text and headings are enough to report on wording. Judging prominence or visual hierarchy needs a rendered view or screenshot.

## 2. Navigation and structure
**Look for:** Number and naming of menu items, whether key pages (contact, pricing, about) are reachable, consistent header and footer, working internal links, helpful page titles and headings.
**Evidence:** Link lists and heading structure from fetched HTML work for structure. "Easy to find" or "confusing" is a usability judgment: present it as a suggestion and recommend a short test with real people.

## 3. Mobile experience
**Look for:** Responsive layout, readable text size, tap-friendly buttons, no horizontal scrolling, menu usability, sticky elements that cover content.
**Evidence:** Needs a rendered view at a mobile-sized viewport (browser emulation or screenshot). A viewport meta tag in the HTML is a hint, not proof the mobile layout works. Emulation is not a real device: say which you used.

## 4. Accessibility
**Look for (from markup):** page language attribute, one logical heading structure, alt text presence on images, form labels, link text that makes sense out of context, landmark elements.
**Look for (needs rendering or tools):** color contrast, visible focus indicators, keyboard operability, zoom and reflow, motion.
**Evidence:** Markup checks can be Observed. Contrast, focus, and keyboard behavior need a browser or tool run. An automated checker only finds a subset of issues; never say a site "is accessible" or "passes" based on one. Full assessment needs keyboard and screen reader testing: list it under Needs testing.

## 5. Trust signals
**Look for:** Clear business identity, contact details, about page, privacy and terms pages, testimonials or case studies (with attribution), security-relevant basics visible to users such as HTTPS in the URL, clear pricing and policies.
**Evidence:** Report what is present or absent on the pages you reviewed. Do not judge authenticity of testimonials or certifications, and do not claim security vulnerabilities from surface observations.

## 6. Calls to action
**Look for:** A clear primary action per key page, descriptive button text, a visible action early on the page, a low-friction path to contact or purchase, and consistent wording.
**Evidence:** Presence and wording from text; prominence and placement need a rendered view. Submitting forms or starting checkout requires the user's explicit approval: otherwise list "test the form end to end" under Needs testing.

## 7. Technical hygiene
**Look for:** Broken links you actually requested, a descriptive title and meta description, social preview tags, redirects to HTTPS, favicon, obvious oversized images, console errors if a browser is available.
**Evidence:** Report only responses you actually received (e.g., a link that returned an error when you requested it, with the date). Do not infer real-world speed from page weight alone, and do not claim performance scores without a tool that produced them. Do not run vulnerability scans.

## 8. Evidence quick-reference

| Claim type | Minimum evidence |
|---|---|
| Wording, headings, link targets | Fetched text/HTML |
| Alt text, labels, lang attribute present or missing | Fetched HTML |
| Broken link | You requested it and got an error response |
| Visual layout, spacing, hierarchy, contrast | Screenshot or rendered view you actually saw |
| Mobile layout | Rendered view at a mobile viewport (state emulated or real) |
| Keyboard or screen reader behavior | A test you actually ran |
| Speed or performance numbers | Output from a named measuring tool |
| Security issues | Do not claim from passive observation; recommend a qualified review |
| User behavior or conversion impact | Not available from an audit; suggest user testing or analytics review |
