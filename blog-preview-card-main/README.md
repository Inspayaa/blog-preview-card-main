Frontend Mentor - Blog preview card solution
This is a solution to the Blog preview card challenge on Frontend Mentor. Frontend Mentor challenges help you improve your coding skills by building realistic projects.

Table of contents
Overview

The challenge

Screenshot

Links

My process

Built with

What I learned

Continued development

Useful resources

AI Collaboration

Author

Overview
The challenge
Users should be able to:

See hover and focus states for all interactive elements on the page

Experience a stepped, neo-brutalist hover animation on the main card

Screenshot
![Blog preview card in MS Edge](<Screenshot (471).png>)
![Blog preview card in MS Edge inspection mode 1440px width](<Screenshot (472).png>)
![Blog preview card in MS Edge inspection mode 375px width(Mobile)](<Screenshot (473).png>)
(Note: Replace ./screenshot.jpg with the actual path to your screenshot)

Links
Solution URL: [GitHub](https://github.com/Inspayaa/blog-preview-card-main.git)

Live Site URL: [Github Pages](https://inspayaa.github.io/blog-preview-card-main/)

My process
Built with
Semantic HTML5 markup

CSS custom properties (Variables)

Flexbox

Vanilla CSS

Advanced CSS Animations (@keyframes)

What I learned
The biggest takeaway from this project was mastering complex CSS animations to create a specific shadow effect. Initially, I tried using standard CSS transition properties, but I realized that transitions only smoothly interpolate between two states.

Here is the CSS I'm most proud of, which creates that rigid, frame-by-frame pop effect:

CSS
.container {
   animation: shadowExit 0.7s ease forwards;
}

.container:hover {
        animation: shadowEnter 0.7s ease forwards;
    .title {
        color: var(--Yellow);
    }
}

@keyframes shadowEnter {
    0%, 25%{
        box-shadow: 5px 5px 0px var(--Gray-950);
    }

    26%, 50%{
        box-shadow: 7px 7px 0px var(--Gray-950b);
    }

    51%, 75%{
        box-shadow: 10px 10px 0px var(--Gray-950b);
    }
    
    76%, 100%{
        box-shadow: 12px 12px 0px var(--Gray-950);
    }
}


@keyframes shadowExit {
    0%, 25% {
        box-shadow: 13px 13px 0px var(--Gray-950);
    }

    26%, 50% {
       box-shadow: 11px 11px 0px var(--Gray-950b);
    }

    51%, 75% {   
       box-shadow: 9px 9px 0px var(--Gray-950b);
    }

    76%, 100% {
        box-shadow: 6px 6px 0px var(--Gray-950);
    }
}

Continued development
Moving forward, I want to continue exploring neo-brutalist design trends and how to push vanilla CSS to handle complex, staged animations without relying on heavy JavaScript libraries. I also plan to focus more on combining transform properties with layout shifts for more tactile user interfaces.

Useful resources
MDN Web Docs: steps() - This documentation was crucial in helping me understand how to force the browser to render animations frame-by-frame instead of smoothly.

MDN Web Docs: Using multiple box-shadows - Helped me understand how to layer a semi-transparent shadow underneath a solid one.

AI Collaboration
I collaborated with an AI assistant to debug and refine my CSS animations.

Goal: I wanted to replicate the very specific layered shadow hover effect I noticed in the Figma file, but my initial transition: box-shadow attempts were too smooth and didn't have the "double shadow" look. Tried using the @keyframes and wasn't getting any closer.

Process: I shared my base CSS with the AI, and we iterated through several solutions. We started with layering hsla and solid colors, moved to @keyframes. I think I was able to replicate something very close to the original. It wasn't easy but was a fun learning process.

Author
Obioma Tobechukwu Joel - @Inspayaa

Linkedin - @[Tobechukwu Joel Obioma](https://www.linkedin.com/in/tobechukwu-joel-obioma-3b3b60183/)

                                😊