# Thursday, March 30th

## Front-end Development

The goal of front-end development is to create an application that the end-user can use intuitively, and contains information that is concise and relevant to what they need.

The goal sounds obvious, but this isn't simple. We use a combination of HTML, CSS, and JavaScript on the web to do typical front-end development, but all of these technologies are constantly changing and conflicting.

Often times, when you've planned to create one site, with one design, you will be surprised when that one design has to adapt to many conflicting technologies.

### Browser Conflicts

For example, if you are designing a new site, and you are using some new CSS3 functionality, the challenge is that some people that use older browsers won't be able to see what you did. Of course you don't need to cater to someone running a 1995 Gateway computer running NetScape or something, but you need to think of who you are supporting, and you need to justify serving a broken site to someone running an old browser.

Now, you will typically define the set of browsers and versions that you support, based on the demographic of who is using your site. If you are creating a business website for an established group of older businesspeople, you might need to support something like Internet Explorer 7, even if that means having to forgo some more modern approaches.

Know your audience.

### Accessibility

Focusing on accessibility is one of the most important things you can do as an ethical developer.

Those who are visually impaired might use a screen-reader, which is a program that will read the content on a page out loud. This program will read the HTML very literally. It will treat the H1 as a page title, and it will allow the user to jump between the content that falls under different H2 tags. **This is why you have to care about semantics, and the established HTML specifications.** If you don't, you have prevented someone with a disability from using your site, and there can be repercussions for that, either legal, financial, or ethical.

Here is a simple example of a situation in which accessibility is important. Say you make a very visual website, and a user is expected to click on links based on color. **What if that user is colorblind or otherwise visually impaired?** You can still have this feature, but you have the responsibility as a developer to answer this question. Maybe you have alt tags that can walk a person using a screen reader through it. Maybe you have a colorblind mode that will change the colors to all grayscale. These things matter, always keep them in mind.

## JQuery

JQuery is a JavaScript library that looks to simplify things. It makes DOM traversal easier (selecting HTML elements, or finding children or parent elements, etc). It also provides an important foundation for front-end development, allowing you to more easily introduce things like fades, moving elements, event handlers (on click, on mouse enter, etc).

You can find out more and see documentation for it here:

https://jquery.com/

### Exercises

I want all of you to see my codepen here:

http://codepen.io/aceslowman/pen/bqQXqm?editors=1011

Complete each of the tasks described in the HTML, using JQuery.

Once this is finished, I want you to also work through these P5 exercises, exploring drawing, loops, and modulus.

1. http://codepen.io/aceslowman/pen/gmZbzj
2. http://codepen.io/aceslowman/pen/MpZwae
3. http://codepen.io/aceslowman/pen/MpZwwe
