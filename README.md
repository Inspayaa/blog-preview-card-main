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

Live Site URL: Add live site URL here

My process
Built with
Semantic HTML5 markup

CSS custom properties (Variables)

Flexbox

Vanilla CSS

Advanced CSS Animations (@keyframes)

What I learned
The biggest takeaway from this project was mastering complex CSS animations to create a specific, mechanical "stepped" shadow effect. Initially, I tried using standard CSS transition properties, but I realized that transitions only smoothly interpolate between two states.

To achieve a snappy, multi-layered shadow that shoots out a transparent preview before turning solid, I learned how to combine stacked box-shadow properties with @keyframes and the steps() timing function to eliminate browser smoothing entirely.

Here is the CSS I'm most proud of, which creates that rigid, frame-by-frame pop effect:

CSS
.container {
    /* Base resting state */
    box-shadow: 6px 6px 0px var(--Gray-950);
    
    /* Using steps(1, end) to completely disable smooth interpolation */
    animation: shadowExit 0.3s steps(1, end) forwards;
}

.container:hover {
    animation: shadowEnter 0.3s steps(1, end) forwards;
}

@keyframes shadowEnter {
    0% {
        box-shadow: 6px 6px 0px var(--Gray-950);
        transform: translate(0, 0);
    }
    /* Instantly snaps to a semi-transparent preview frame */
    33% {
        box-shadow: 
            6px 6px 0px var(--Gray-950),
            14px 14px 0px hsla(0, 0%, 7%, 0.25);
        transform: translate(-2px, -2px);
    }
    /* Instantly snaps to the solid final frame */
    66%, 100% {
        box-shadow: 12px 12px 0px var(--Gray-950);
        transform: translate(-2px, -2px);
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