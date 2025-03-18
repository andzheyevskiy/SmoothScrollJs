# SmoothScrollJs

JavaScript library designed to implement smooth scrolling functionality for web projects.

## Installation

You can install SmoothScrollJs via npm:

```bash
npm install git+https://github.com/andzheyevskiy/SmoothScrollJs.git
```

## Usage

To use SmoothScrollJs in your project, you need to import and initialize it. Here is an example:

```javascript
import smoothScroll from 'smooth-scroll-js';

// Initialize SmoothScroll with default options
smoothScroll('#target');

// You can also customize options
smoothScroll('#target', {
  duration: 800, // Duration of the scrolling animation in milliseconds (default: 500)
  easing: 'easeInOutCubic', // Easing pattern to use (default: 'easeInOutQuad')
  offset: 0, // Offset in pixels to be added to the target's position (default: 0)
});
```

### Parameters

- **`target`** `{string | HTMLElement}`  
  The target element to scroll to. Can be a CSS selector or an `HTMLElement`.

- **`options`** `{Object} [optional]`  
  Optional configuration object with the following properties:

  - **`duration`** `{number} [default: 500]`  
    Duration of the scroll animation in milliseconds.

  - **`offset`** `{number} [default: 0]`  
    Offset in pixels.  
    - Positive values will stop the scroll before the target reaches the top.  
    - Negative values will scroll past the target.

  - **`easing`** `{string} [default: 'easeInOutQuad']`  
    The easing function to use for the animation.  
    Possible values:  
    - `'linear'`  
    - `'easeInQuad'`  
    - `'easeOutQuad'`  
    - `'easeInOutQuad'`

### Exceptions

Throws an error in the following cases:

- If `target` is not a `string` or `HTMLElement`.
- If `duration` is not a `number`.
- If `offset` is not a `number`.
- If `easing` function is not a `string`.

## License

This project is licensed under the MIT License. See the [LICENSE](LICENSE) file for details.
