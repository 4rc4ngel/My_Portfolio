# My_Portfolio

I had the idea to create a portfolio page showcasing my ability to design and layout web apps to potential employers, I wanted my web app to be clean and summarise procedures I use when developing, then have a section that showcases the type of apps I’ve already completed. I also want the user to view my progress in the tech stack, followed by a simple business type card effect alongside a form. 

Along with the option to download my CV.

## UX

I used some ideas from the 5 planes of design, I thought deeply about what the goals to my web app are. Who will want to view it and what type of feeling I wanted to invoke?

I looked through other portfolio type pages to gain inspiration, a key element at this stage was to try and keep things simple, clean layout where I could demonstrate ability yet keep within the confines of my current skill level. 

I then moved on to balsamiq to begin [wireframing my idea.](https://github.com/4rc4ngel/user_centric_frontend_project/blob/master/Portfolio%20Website.pdf) This really helped when it comes to begin writing the code, to have that idea to keep referring to made things a lot simpler. 

I liked the idea of adding accent colour to key words, I remembered reading somewhere that the colour 
> Green invokes a calming sensation. 

So, opted for the hex colour `#a2f1a1` I then used this colour across my theme, highlighting titles and key words I wanted to stand out. 

Towards the end of my development, I realised I’d left out an integral section which would contain my contact details.  I created this section on the fly, completely changing the original. I also added a CV link and download icon into the nav bar.

I also selectd background images which subtley linked to each section. 

Overall, I’m happy with how the colour `#a2f1a1` contrasts with bootstraps dark backgrounds.

## Features

My current skill level dictates that I should keep my app simple. 

I wanted no more than 5 sections: -

1. **Main Title Area**, with a strap line on **Design, Create, Code** the core fundamentals of Full Stack development
2. **About Me**, which tied in the strap line, **Design, Create, Code** concept and expanded on my development process.
3. **Projects Section** was to simply provide a snapshot of projects I’ve completed. Just to give the user the idea I can create different types of apps and not just static pages.
4. **Progress Section**, I was mindful of separating the front end an backend and so subtly ordered the progress bars in this manner. 
5. **Contact section**, I wanted to keep this simple, a floating looking business card and a form which has some limited validation. 

Starting with the Nav, I felt bootstraps standard hamburger type Nav would suffice for my web app, I added a little opacity to the navbar, so when using in mobile mode the dropdown doesn't obscure the main content.

There's a link in the nav which points to my CV. The Images on the projects section are clickable and open a modal to view a large version of the card image.

I used 3 fixed backgrounds to give a parlax scrolling effect, and created overlays for each to prevent the titles and sub headings being lost. 

My prgress bar area, uses the logo colors of each technology to further identify with the product. 

Each social icon is styled with a hover effect of its companies’ logo colour. 

## Technologies Used

My project used 

- HTLM5 for Semantic Mark-up 
- CSS3 for styling
- [Bootstrap](https://getbootstrap.com/) is used to achieve layout.
- [jQuery](https://jquery.com/) is used to achieve, scroll spy and smooth scrolling effect.
- [PopperJS](https://popper.js.org/) is used to achieve the modal effect.
- [Font-Awesome](https://fontawesome.com/) was used to render the icons in the about section and the download CV icon. 
- Full screen capture a Google Chrome extension was used to capture full length of web apps showcased in the projects section.
- All my code was written with visual studio code and live server, so I could visualise updates in real time. 



## Testing 

I extensively tested my sites responsiveness, using Chrome Developer tools. Initially while the site was responsive there were some layout issues. 

1. The heading title at medium to small screen sizes didn’t wrap how I wanted and there was too much top padding
   1. I created a media query `max-width: 1199px` and made the heading a `flex` container to ensure the accented part of the main heading dropped onto its own level on medium to small screens. 
   2. reduced `padding-top` on both `max-width: 1199px` and `max-width: 769px` media queries.
   3. reduced the `#main-section` height and overlay height for medium to small screens.

  
3. I didn't like the `font-size` for any of the subtitles on medium to small screens.
    1. Created 2 x media queries `max-width: 1199px` and `max-width: 769px;` to shrink the subtitles at both break points.
4. After deploying I retested the site again, only to find that the **bootstrap.js & jquery.js** were not loading, as I initially used static files for in development, I suspected there was an issue with static JavaScript files hosting via GitHub Pages. therefore, made the decision to provide these services via a CDN.
    1. At a later stage I’d like to re-implement the static versions of these services, in case the cdn servers ever went down.
5. After deployment testing another error occurred where my modal images weren't loading.
    1. After some investigation, I had a leading `/` at the beginning of my img reference.  I simply deleted these leading `/` and redeployed to GitHub Pages achieving the results I desired.
    
6. I ran both HTML and CSS files through a code Validator with no errors.
    
## Deployment

When I was finally happy with my site, it was time to deploy to GitHub pages. I chose this hosting as it's perfect for hosting single page applications, as mentioned previously, I hit a bug in testing after development where the static JavaScript files were not being located, so rectified this using CDN's.

The process of deployment was quite simple, I navigated to the settings area in my repository and scrolled down to the GitHub Pages section, it asks where you would like to host the source from and I selected the master branch of my repository. Within moments my site was hosted at [Portfolio]( https://4rc4ngel.github.io/user_centric_frontend_project/)

## Credits


### Content

All the content provided is my own. 

### Media
- The background images were sourced from [pixabay](https://pixabay.com/)

### Acknowledgments 
- Traversy Media, Tutorial implementing **scrollspy** and **Smooth Scroll**
