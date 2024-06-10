# loader-in-Pure-CSS
A code repo for a Pure CSS Loader

This code creates a loader animation using HTML and CSS. The loader consists of five vertical bars that change their opacity and scale up in height in a staggered sequence, creating a visual effect of movement.

Here's a detailed breakdown of how the code works:

-> HTML Explanation:
* The div element with the class loader contains five span elements each with the class loader_bar.
* Each span element has an inline style that sets a CSS variable --d to different values, representing the delay for the animation in milliseconds.

-> CSS Explanation:
* background: black;: Sets the background color of the page to black.
* display: flex; justify-content: center;: Centers the loader horizontally.
* height: 50vh;: Sets the height of the body to 50% of the viewport height, which helps in vertically centering the loader.

=> Loader Container: 
* display: inline-flex; align-items: center; column-gap: 5px;: Aligns the span elements horizontally with equal spacing of 5px between them.

=> Loader Bars:
*display: inline-block;: Allows the span elements to behave like inline elements but with block element properties.
* width: 3px; height: 10px;: Sets the initial size of the loader bars.
* background-color: #fff;: Sets the color of the bars to white.
* opacity: 0.5;: Sets the initial opacity of the bars to 50%.
* border-radius: 10px;: Gives the bars rounded corners.
* animation: scale-up 1000ms var(--d) linear infinite;: Applies the scale-up animation with a duration of 1000ms, a delay specified by the --d variable, a linear timing function, and repeats infinitely.

=> Different Heights for Specific Bars:
* nth-child(even): Selects the even-numbered bars (2nd and 4th) and sets their height to 25px.
* nth-child(3): Selects the 3rd bar and sets its height to 40px.

=> Keyframes for the Animation:
* @keyframes scale-up: Defines the scale-up animation.
* 25% { opacity: 1; scale: 1 1.5; }: At 25% of the animation, the bar becomes fully opaque and scales up vertically by 1.5 times.
* 50% { scale: 1; }: At 50% of the animation, the bar returns to its original size.

-> Summary:

This loader animation involves five bars of varying heights that scale up and down in a staggered manner, giving a pulsating effect. The staggered delay is controlled via the --d CSS variable, making the animation visually engaging and smooth.
