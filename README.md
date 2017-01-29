# Finimize Web Article Solution


## Brief

> Come up with the concept for, and develop, a redesign for our news article pages. Your goal is
to design a page that would increase the conversion of site visitors to newsletter subscribers.
This should be built using Bootstrap. You can use this story as a resource for content.
The page must satisfy the following Acceptance Criteria (ACs) in order of importance:
1. It should allow the user to see the article’s content, header image, date, and readin
time
2. It should entice and have a method for the user to sign up for the Finimize daily email
(not expecting any sign up form to be functional)
3. The actual story text / content should be static in this implementation (no API/dynamic work expected)
4. It should allow the user to see other related stories on the page
5. It should allow the user to share the story on social networks
6. It should include a section for the user to add a comment (can be placeholder)


## Solution Workflow

1. Analyse current article page design
2. Identified unsatisfied ACs
3. Analyse current *email article design*
4. Research/analyse several online blogs/newsletters
5. Write out several ideas for enhancement.
6. Build high def wireframe in Illustrator.
7. Create boilerplate html page with bootstrap.
8. Import assets (example article text, images) and add bootstrap classes (and custom classes).

## Summary

Enhancement ideas were inspired by a mix of email design features and a footer on [treehouse's sign up page](https://teamtreehouse.com/join/start-trial);
1. Add date/read-time to top of page, visible on page load.
2. Add header image below main title.
3. Give article headers a higher font weight.
4. Increase size of social icons and add 'SHARE THIS' aside.
5. Wrap 'related' article content in a card with bold title.
6. Add fixed footer that fades in when user reaches end of article, with a subscribe button.

I created a B/W wireframe (tablet width) in Illustrator loosely based on the proportions of components on the current article pages, working against two central vertical grid lines.
I imported the logo assets in and copied some article text from a finimize email, and added a few screenshots of social icons,
comment fields etc as placeholder content. I analysed the two fonts (Avenir Next and Helvetica) used on the current article pages set body text to Helvetica and Avenir Next to headings. Below the main footer, I added the fixed footer and used the same background colour as the email-articles header (#4EB9E7), and spent a bit of time trying to think of a punchy and enticing way to say 'please sign up for free'. I opted for 'want more? get free daily emails', then added a white button to the right side with 'subscribe'.

I used a boilerplate bootstrap template to set up some basic components and started building a live prototype. I also linked two fonts from google (*Nunito* as fallback for Avenir Next, *Open Sans* as Helvetica fallback).
Many of the assets were pasted in place, and a bit of css was use to override styles in bootstrap and define custom sizes/colours (conscious of time, I choose to work on top of hard coded minified bootstrap css/js, without messing with a preprocessor like sass).

After experimenting and settling on the styles/layout of the main page (with smaller fonts & shallower padding rules for mobile view), I added the enticing footer to the end of the page with a disabled button in place, fixed it, and added some inline JS to the bottom of the document to import the *waypoints* library, then set a rule to fade in the footer when the **share section** becomes visible to the reader (assumes the user has reached the end of the article before the footer appears). I also added css to hide the 'get free daily emails' text on mobile view (and decreased vertical padding) to account for smaller screen size.
