# Accessibility

All of our digital services must be accessible and inclusive to everyone who needs them.

> We must research, design, develop and test according to [GOV.UK guidance](https://www.gov.uk/service-manual/helping-people-to-use-your-service/making-your-service-accessible-an-introduction).

Underpinning this guidance are the [Web Content Accessibility Guidelines (WCAG) version 2.1](https://www.w3.org/WAI/standards-guidelines/wcag/glance/) which we must follow to levels A and AA. These help us ensure that people with a wide range of needs, including people who use assistive technologies, are likely to be able to use our services.

Internal services must also be accessible. Approximately 10% of civil servants who have declared their disability status have a disability. [Accessibility guidance for internal services​](https://www.gov.uk/service-manual/design/services-for-government-users#accessibility)

Accessibility should always be built in from the early designs of a service. It is much more expensive to retrofit accessibility later on, as any issues introduced at the early stages will have propagated across the service.

Good accessibility is not just for people with disabilities. It makes the whole service easier for everyone. For example, it can help you submit a form quickly by pressing Enter, or make a keyboard with an "@" sign appear on your phone when typing in an email address.

## Testing for accessibility

[GOV.UK - testing for accessibility](https://www.gov.uk/service-manual/technology/testing-for-accessibility)

The following checklist maps a full set of tests to the Web Content Accessibility Guidelines:

> [Accessibility checklist](accessibility_checklist.md)

Rather than testing for accessibility at the end of a project, you should always quality assure (QA) the early designs up front. While prototypes do not need to be held to the same standards as production code, look out for accessibility issues which could propagate into development.

A set of default acceptance criteria for development has been suggested by the cross-government accessibility community:

1. Works with keyboard only.
2. Works with one screen reader. Check forms, headings and links as a minimum on each page.
3. Zoom page to 200% - is content still legible?

Then use an automated checker, such as the [WAVE extension](https://wave.webaim.org/extension/) for Chrome or Firefox, for the following:

4. No major issues flagged by the tool.
5. Works without CSS (Cascading Stylesheets) - does content make sense and appear in a logical order?

(Automated checkers help to identify around 30% of accessibility issues, such as insufficient contrast or unlabelled form fields.)

Once you have eliminated major accessibility issues by testing in these ways, the best insight you can get is by doing research with people who use assistive technologies.

## Assistive technologies

Many people with access needs use assistive technology. GOV.UK has a [testing with assistive technologies](https://www.gov.uk/service-manual/technology/testing-with-assistive-technologies) page with a list of the technologies our services need to work against.

You should familiarise yourself with how a screen reader works to help understand how you should mark up and test your web pages. Two free screen readers are:

* [NVDA](https://www.nvaccess.org/) for PC
* [VoiceOver](https://www.apple.com/uk/accessibility/mac/vision/), built into Mac.

[WebAIM](https://webaim.org/) is a great, neutral source on web accessibility and contains cheat sheets for the main assistive technologies.

## Recommended reading and viewing

* ["Designing for accessibility" posters](https://github.com/UKHomeOffice/posters/blob/master/accessibility/dos-donts/posters_en-UK/accessibility-posters-set.pdf): Very popular set of posters on accessibility
* [GOV.UK requirements for public sector sites](https://www.gov.uk/guidance/accessibility-requirements-for-public-sector-websites-and-apps)
* [WebAIM guidance on web accessibility testing](https://webaim.org/resources/evalquickref/)
* [Microsoft's Inclusive 101 guide](https://www.microsoft.com/design/inclusive/)
* [Experiences from an assistive technology user in government](https://accessibility.blog.gov.uk/2016/07/01/accessibility-and-me-chris-moore/)
* [Videos by assistive technology users](http://digitalaccessibilitycentre.org/index.php/videos) from the Digital Accessibility Centre

## Training

Defra colleagues have attended the following courses and found them useful:

* [Upcoming government training](https://designnotes.blog.gov.uk/events-and-training-in-the-user-centred-design-community/) including the Introduction to Accessibility
* [Introduction to web accessibility by Webcredible](https://www.webcredible.com/training/web-accessibility-training/)
* [Udacity: web accessibility course](https://eu.udacity.com/course/web-accessibility--ud891) (free online course for those with a grounding in HTML, CSS and Javascript)

## More links

* [What's new in WCAG 2.1](https://www.w3.org/WAI/standards-guidelines/wcag/new-in-21/)
* [Léonie Watson's blog](https://tink.uk/) - regular insights from a web accessibility expert
* [GOV.UK blog - testing the world's least-accessible webpage](https://accessibility.blog.gov.uk/2017/02/24/what-we-found-when-we-tested-tools-on-the-worlds-least-accessible-webpage/)
* [The A11y Project](https://a11yproject.com/): A community-driven effort to make web accessibility easier
* [Randoma11y](https://www.randoma11y.com/#/?_k=olul7y): Random accessible colour palette generator
