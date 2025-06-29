# **AI Prompt: Generate the "Liquid Glass" UI Theme**

## **Objective**

Your task is to generate the complete front-end code (HTML and CSS, or for a framework like React/Vue/Svelte) for a cohesive UI component library based on the **"Liquid Glass"** theme. This theme is defined by its use of translucent, frosted glass-like elements, fluid animations, and a strong sense of depth and light.

## **Core Principles**

1.  **Translucency & Frosted Glass:** The core material for most components is a semi-transparent element with a blurred backdrop (`backdrop-filter: blur()`). This creates a frosted glass effect, allowing the background to be visible but indistinct.
2.  **Depth & Elevation:** Components should feel like they are floating in space. Use soft, diffused shadows (`box-shadow`) and subtle borders (`border: 1px solid rgba(...)`) to lift elements off the page. Interactive elements should appear closer to the user on hover.
3.  **Liquid & Light Animations:** All interactions must be fluid, responsive, and organic. Animations should mimic the properties of liquid, light, and physics. Use smooth transitions (`transition`), ease-in-out timing functions, and subtle glows.
4.  **Minimalism & Clarity:** Despite the complex effects, the design must remain clean and uncluttered. Prioritize typography, generous spacing, and a clear visual hierarchy.

---

## **Theme Styles**

*   **Light Theme:** Use a bright, subtly-graded background. Glass elements should be a light, milky white with low opacity (`rgba(255, 255, 255, 0.1)`). Shadows are soft and light gray. Text is a high-contrast dark color (e.g., `#111`).
*   **Dark Theme:** Use a dark, deep-colored background (e.g., near-black, deep blue/purple). Glass elements have a darker tint (`rgba(10, 10, 20, 0.2)`). Illumination is key: use soft, glowing highlights (`box-shadow`) and vibrant accent colors that appear to emanate from within the components. Text is a bright, luminous color (e.g., `#efefef`).

---

## **Component Specification**

For every component below, provide the style and animation details consistent with the "Liquid Glass" theme.

### **Accordion**
*   **Style:** Each item is a floating glass panel with rounded corners. The header is separated from the content by a subtle internal divider. A chevron icon indicates the state.
*   **Animation:** The chevron smoothly rotates on open/close. The content panel expands and collapses with a fluid, easing motion, as if filling with liquid.
*   **Code:**
    ```css
    .accordion-item {
      background: rgba(255, 255, 255, 0.1);
      backdrop-filter: blur(20px);
      border-radius: 12px;
      border: 1px solid rgba(255, 255, 255, 0.2);
      margin-bottom: 10px;
      transition: all 0.4s ease-in-out;
    }
    .accordion-header:hover { background: rgba(255, 255, 255, 0.2); }
    ```

### **Alert**
*   **Style:** A floating glass panel. A vertical, glowing bar on the left side indicates its status (e.g., green for success, red for error). The icon and text are crisp.
*   **Animation:** The alert slides smoothly into view. When dismissed, it fades and shrinks away.
*   **Code:**
    ```css
    .alert-success {
      background: rgba(46, 204, 113, 0.15);
      backdrop-filter: blur(15px);
      border-left: 4px solid rgba(46, 204, 113, 1.0);
      box-shadow: 0 0 20px rgba(46, 204, 113, 0.3);
    }
    ```

### **Avatar**
*   **Style:** The image is housed in a circular glass frame. A subtle, glowing border can indicate user status (green for online, gray for offline).
*   **Animation:** On hover, the avatar gently lifts (`transform: translateY(-2px)`) and a soft light diffuses behind it.
*   **Code:**
    ```css
    .avatar-frame {
      background: rgba(255, 255, 255, 0.1);
      backdrop-filter: blur(10px);
      border-radius: 50%;
      padding: 4px;
      border: 2px solid rgba(46, 204, 113, 0.8); /* Online status */
    }
    ```

### **Badge**
*   **Style:** A small, pill-shaped piece of polished, translucent glass. The color reflects its purpose. The text/number inside has a soft, inner glow.
*   **Animation:** When a value changes, the badge subtly pulses with light.
*   **Code:**
    ```css
    .badge {
      background: rgba(220, 53, 69, 0.25);
      backdrop-filter: blur(5px);
      border-radius: 20px;
      color: white;
      text-shadow: 0 0 5px rgba(255, 255, 255, 0.5);
    }
    ```

### **Breadcrumbs**
*   **Style:** Text links separated by a glowing dot or a very faint glass pipe character (`|`). The current page is opaque text, while links are translucent.
*   **Animation:** On hover, the link's text illuminates and becomes fully opaque.
*   **Code:**
    ```css
    .breadcrumb-link { color: rgba(255, 255, 255, 0.7); transition: color 0.3s ease; }
    .breadcrumb-link:hover { color: rgba(255, 255, 255, 1.0); }
    .breadcrumb-separator { color: rgba(255, 255, 255, 0.4); margin: 0 8px; }
    ```

### **Button**
*   **Style:** A floating glass panel. Primary buttons have a shimmering gradient.
*   **Animation:** Lifts and brightens on hover. On click, the surface depresses with a liquid ripple effect emanating from the point of contact.
*   **Code:**
    ```css
    .button {
      background: rgba(255, 255, 255, 0.1);
      backdrop-filter: blur(12px);
      border: 1px solid rgba(255, 255, 255, 0.2);
      border-radius: 10px;
      transition: all 0.3s ease;
    }
    .button:hover {
      transform: translateY(-3px);
      box-shadow: 0 8px 20px rgba(0, 0, 0, 0.2);
      background: rgba(255, 255, 255, 0.2);
    }
    ```

### **Calendar / Date Picker / Date Range Picker**
*   **Style:** The main container is a large glass panel. Days are individual glass squares. Today's date has a subtle glowing border. The selected day/range is a solid, glowing color fill.
*   **Animation:** Month transitions slide or fade smoothly. Hovering over a day causes it to gently illuminate.
*   **Code:**
    ```css
    .calendar-day { transition: background 0.3s ease; }
    .calendar-day:hover { background: rgba(255, 255, 255, 0.1); }
    .calendar-day-selected { background: rgba(52, 152, 219, 0.5); }
    .date-range { background: rgba(52, 152, 219, 0.2); }
    ```

### **Card**
*   **Style:** A fundamental surface for content. A large panel of frosted glass with rounded corners and a soft, 1px border.
*   **Animation:** On hover, the card tilts slightly towards the cursor for a 3D parallax effect.
*   **Code:**
    ```css
    .card {
      background: rgba(255, 255, 255, 0.05);
      backdrop-filter: blur(30px);
      border-radius: 16px;
      border: 1px solid rgba(255, 255, 255, 0.1);
      transition: all 0.4s ease;
    }
    ```

### **Checkbox / Checkbox Group**
*   **Style:** The checkbox is a square glass container. When checked, a sphere of liquid color animates to fill it. A checkbox group can be enclosed in a larger, recessed glass panel.
*   **Animation:** The fill animation is fluid with a slight "overshoot" bounce.
*   **Code:**
    ```css
    .checkbox-box {
      border: 2px solid rgba(255, 255, 255, 0.3);
      border-radius: 6px;
      transition: all 0.3s ease;
    }
    .checkbox-box:checked {
      background: rgba(52, 152, 219, 0.5);
      border-color: rgba(52, 152, 219, 0.8);
    }
    ```

### **Chip**
*   **Style:** A small, pill-shaped glass element representing an attribute or input. Can contain a dismiss icon.
*   **Animation:** On hover, it lifts slightly. The dismiss icon has a ripple effect on click.
*   **Code:**
    ```css
    .chip {
      display: inline-flex;
      align-items: center;
      background: rgba(255, 255, 255, 0.1);
      backdrop-filter: blur(10px);
      border-radius: 20px;
      padding: 4px 10px;
    }
    ```

### **Circular Progress**
*   **Style:** A ring of liquid glass that fills with a glowing, vibrant color. For indeterminate state, a shimmering highlight endlessly rotates around the ring.
*   **Animation:** The fill animates smoothly around the circle.
*   **Code:**
    ```css
    .circular-progress-fill {
      stroke: url(#gradient); /* Use SVG gradient for liquid feel */
      stroke-linecap: round;
      transition: stroke-dashoffset 0.5s ease-in-out;
    }
    ```

### **Code / Snippet**
*   **Style:** A glass panel with a darker, less transparent background for better readability. Syntax highlighting should use neon-like, glowing colors. A snippet is the inline version.
*   **Animation:** A copy button on the container can produce a success glow.
*   **Code:**
    ```css
    .code-block {
      background: rgba(0, 0, 0, 0.2);
      backdrop-filter: blur(25px);
      border-radius: 8px;
      padding: 16px;
    }
    .token.keyword { color: #ff79c6; text-shadow: 0 0 5px #ff79c6; }
    ```

### **Divider**
*   **Style:** A thin, frosted glass line (1-2px thick) with a soft, ethereal glow. It should feel like a subtle fissure of light.
*   **Animation:** Can subtly brighten on page load.
*   **Code:**
    ```css
    .divider {
      height: 1px;
      background: rgba(255, 255, 255, 0.2);
      box-shadow: 0 0 10px rgba(255, 255, 255, 0.1);
    }
    ```

### **Drawer**
*   **Style:** A large glass panel that slides in from an edge of the screen, blurring the content it covers.
*   **Animation:** Slides in smoothly with an ease-out timing function.
*   **Code:**
    ```css
    .drawer {
      background: rgba(10, 10, 20, 0.2);
      backdrop-filter: blur(40px);
      box-shadow: -10px 0 30px rgba(0, 0, 0, 0.2);
    }
    ```

### **Form / Input / Number Input / Text Area / Date Input / Time Input**
*   **Style:** All inputs are recessed, frosted glass troughs. When focused, a glowing border animates around the input. Placeholder text is translucent. Text Area is a larger, resizable version.
*   **Animation:** The border glow fades in smoothly on focus.
*   **Code:**
    ```css
    .input {
      background: rgba(0, 0, 0, 0.1);
      border: 1px solid rgba(255, 255, 255, 0.2);
      border-radius: 8px;
      transition: all 0.3s ease;
    }
    .input:focus {
      outline: none;
      border-color: rgba(52, 152, 219, 0.8);
      box-shadow: 0 0 15px rgba(52, 152, 219, 0.4);
    }
    ```

### **Input OTP**
*   **Style:** A series of individual input boxes. The active input has a brighter, pulsing glow.
*   **Animation:** Focus jumps automatically to the next box, carrying the glow with it.
*   **Code:**
    ```css
    .otp-input:focus {
      transform: scale(1.1);
      box-shadow: 0 0 25px rgba(52, 152, 219, 0.6);
    }
    ```

### **Image**
*   **Style:** The image is housed within a glass frame with a subtle border.
*   **Animation:** On hover, the frame illuminates and the image inside may gain a slight parallax depth effect.
*   **Code:**
    ```css
    .image-frame {
      border-radius: 12px;
      padding: 8px;
      background: rgba(255, 255, 255, 0.05);
      border: 1px solid rgba(255, 255, 255, 0.1);
      transition: all 0.3s ease;
    }
    .image-frame:hover { box-shadow: 0 0 20px rgba(255, 255, 255, 0.1); }
    ```

### **Keyboard Key**
*   **Style:** A small, 3D-looking glass key that appears to float.
*   **Animation:** Depresses with a soft glow on click/press.
*   **Code:**
    ```css
    .kdb-key {
      background: rgba(255, 255, 255, 0.1);
      border: 1px solid rgba(255, 255, 255, 0.2);
      border-radius: 6px;
      box-shadow: 0 2px 0 rgba(255, 255, 255, 0.2);
    }
    .kdb-key:active { transform: translateY(1px); box-shadow: 0 1px 0 rgba(255, 255, 255, 0.2); }
    ```

### **Link**
*   **Style:** Does not have a glass background. The text itself is the interactive element.
*   **Animation:** On hover, the text gains a subtle, shimmering gradient effect, as if light is flowing through it.
*   **Code:**
    ```css
    .link {
      background: linear-gradient(90deg, #A0C4FF, #BDB2FF);
      -webkit-background-clip: text;
      -webkit-text-fill-color: transparent;
      transition: filter 0.4s ease;
    }
    .link:hover { filter: brightness(1.5); }
    ```

### **Listbox**
*   **Style:** A container like a dropdown menu. Each item is a separate glass panel.
*   **Animation:** Hovered items illuminate. Selected items have a persistent, soft glow. Animates in with a subtle fade and scale.
*   **Code:**
    ```css
    .listbox-item[aria-selected="true"] {
      background: rgba(52, 152, 219, 0.2);
      box-shadow: inset 0 0 10px rgba(52, 152, 219, 0.3);
    }
    ```

### **Modal**
*   **Style:** A large, floating pane of glass in the screen's center. The page background darkens and blurs significantly to focus attention.
*   **Animation:** Fades and scales up from the center with a slight "settle" bounce.
*   **Code:**
    ```css
    .modal-content {
      background: rgba(255, 255, 255, 0.1);
      backdrop-filter: blur(40px);
      border: 1px solid rgba(255, 255, 255, 0.2);
    }
    .modal-overlay { background: rgba(0, 0, 0, 0.3); backdrop-filter: blur(10px); }
    ```

### **Navbar**
*   **Style:** A long, horizontal glass panel fixed to the top. It's semi-transparent, allowing page content to blur behind it on scroll.
*   **Animation:** Can become slightly less transparent or gain a stronger shadow on scroll to maintain visibility.
*   **Code:**
    ```css
    .navbar {
      position: sticky; top: 0;
      width: 100%;
      background: rgba(10, 10, 20, 0.2);
      backdrop-filter: blur(30px);
      transition: background 0.3s ease;
    }
    ```

### **Pagination**
*   **Style:** Each page number is a small glass circle or square. The active page is larger, brighter, and has a prominent glow.
*   **Animation:** Hovering over a page number causes it to lift and glow.
*   **Code:**
    ```css
    .pagination-item-active {
      background: rgba(52, 152, 219, 0.5);
      box-shadow: 0 0 15px rgba(52, 152, 219, 0.5);
      transform: scale(1.1);
    }
    ```

### **Popover**
*   **Style:** A small, floating glass bubble that appears on demand, often tied to another element.
*   **Animation:** Appears with a soft "pop" (scale and fade-in) animation.
*   **Code:**
    ```css
    .popover {
      background: rgba(50, 50, 50, 0.3);
      backdrop-filter: blur(30px);
      border-radius: 12px;
      border: 1px solid rgba(255, 255, 255, 0.1);
    }
    ```

### **Progress**
*   **Style:** The track is a recessed, semi-transparent glass channel. The fill is a vibrant, glowing liquid.
*   **Animation:** A shimmering highlight continuously sweeps across the filled portion.
*   **Code:**
    ```css
    .progress-fill {
      background: linear-gradient(90deg, #3498db, #8e44ad);
      box-shadow: 0 0 15px #3498db;
    }
    ```

### **Radio Group**
*   **Style:** Each radio button is a glass circle. When selected, a liquid sphere animates into the center.
*   **Animation:** The inner sphere animates in with a quick, fluid pop.
*   **Code:**
    ```css
    .radio-dot {
      transform: scale(0);
      background: white;
      transition: transform 0.3s ease;
    }
    .radio-input:checked + .radio-label .radio-dot { transform: scale(1); }
    ```

### **Scroll Shadow**
*   **Style:** Instead of a harsh shadow, use a frosted glass gradient at the top/bottom of a scrollable container to indicate more content.
*   **Code:**
    ```css
    .scroll-container {
      -webkit-mask-image: linear-gradient(black, black, transparent),
                          linear-gradient(transparent, black, black);
      -webkit-mask-position: top, bottom;
    }
    ```

### **Skeleton**
*   **Style:** A glass shape placeholder for loading content.
*   **Animation:** A soft, shimmering wave of light continuously sweeps across the component.
*   **Code:**
    ```css
    .skeleton::after {
      content: ''; position: absolute; top: 0; left: -150%;
      width: 150%; height: 100%;
      background: linear-gradient(90deg, transparent, rgba(255, 255, 255, 0.1), transparent);
      animation: shimmer 1.5s infinite;
    }
    @keyframes shimmer { 100% { left: 150%; } }
    ```

### **Slider**
*   **Style:** The track is a recessed glass channel. The thumb is a polished glass sphere.
*   **Animation:** The thumb has a soft glow that intensifies when dragged. It glides smoothly along the track.
*   **Code:**
    ```css
    .slider-thumb {
      background: white;
      border-radius: 50%;
      box-shadow: 0 0 15px rgba(255, 255, 255, 0.5);
    }
    ```

### **Spacer**
*   **Style:** This is a purely functional component for creating space; it has no visual style.

### **Spinner**
*   **Style:** A ring of liquid glass with a gap, rotating endlessly. Or, several small glass orbs rotating in a circle, leaving faint light trails.
*   **Animation:** Smooth, continuous rotation with an ease-in-out curve.
*   **Code:**
    ```css
    .spinner {
      border: 4px solid rgba(255, 255, 255, 0.2);
      border-top-color: white;
      border-radius: 50%;
      animation: spin 1s linear infinite;
    }
    @keyframes spin { 100% { transform: rotate(360deg); } }
    ```

### **Switch**
*   **Style:** The track is a pill-shaped glass channel. The thumb is a polished glass sphere. When 'on', the track fills with a soft, glowing color.
*   **Animation:** The thumb slides smoothly. The background color flows in like liquid.
*   **Code:**
    ```css
    .switch-track[aria-checked="true"] { background: rgba(46, 204, 113, 0.5); }
    .switch-thumb {
      background: white;
      box-shadow: 0 2px 8px rgba(0, 0, 0, 0.3);
    }
    ```

### **Table**
*   **Style:** The container is a large glass panel. Headers are in a slightly raised glass bar. Rows are separated by thin, glowing divider lines.
*   **Animation:** Hovering over a row causes it to light up with a soft, uniform glow.
*   **Code:**
    ```css
    .table-row { transition: background 0.3s ease; }
    .table-row:hover { background: rgba(255, 255, 255, 0.1); }
    .table-divider { border-color: rgba(255, 255, 255, 0.1); }
    ```

### **Tabs**
*   **Style:** The active tab is a distinct liquid glass panel encapsulating the label. Inactive tabs are translucent text.
*   **Animation:** The active glass panel slides fluidly from the old tab to the new one, morphing its width to fit the new label.
*   **Code:**
    ```css
    .tab-active-indicator {
      position: absolute; height: 100%;
      background: rgba(255, 255, 255, 0.15);
      backdrop-filter: blur(10px);
      border-radius: 8px;
      transition: all 0.4s cubic-bezier(0.23, 1, 0.32, 1);
    }
    ```

### **Tooltip**
*   **Style:** A small, dark glass bubble that appears on hover. Text inside is bright and clear.
*   **Animation:** Fades in and moves slightly away from the parent element.
*   **Code:**
    ```css
    .tooltip {
      background: rgba(20, 20, 20, 0.5);
      backdrop-filter: blur(15px);
      border-radius: 6px;
      color: white;
    }
    ```

### **User**
*   **Style:** Combines the "Avatar" and text labels (name, username).
*   **Animation:** On hover, a faint glass background can appear behind the entire component to group the elements, and it can lift slightly.

```example_html
<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Liquid Glass UI Component Showcase</title>
    <style>
        /* ------------------------- */
        /* --- CORE & THEME --- */
        /* ------------------------- */

        :root {
            --font-family: -apple-system, BlinkMacSystemFont, "Segoe UI", Roboto, Helvetica, Arial, sans-serif, "Apple Color Emoji", "Segoe UI Emoji", "Segoe UI Symbol";
            
            /* Light Theme */
            --bg-light: #f0f2f5;
            --bg-gradient-light: linear-gradient(135deg, #e6e9f0 0%, #eef1f5 100%);
            --text-color-light: #1c1c1e;
            --glass-bg-light: rgba(255, 255, 255, 0.2);
            --glass-border-light: rgba(255, 255, 255, 0.3);
            --glow-light: rgba(0, 122, 255, 0.5);
            --shadow-light: rgba(0, 0, 0, 0.1);

            /* Dark Theme */
            --bg-dark: #121212;
            --bg-gradient-dark: linear-gradient(135deg, #1f2128 0%, #121212 100%);
            --text-color-dark: #e1e1e1;
            --glass-bg-dark: rgba(25, 25, 35, 0.2);
            --glass-border-dark: rgba(255, 255, 255, 0.1);
            --glow-dark: rgba(0, 196, 255, 0.6);
            --shadow-dark: rgba(0, 0, 0, 0.3);

            /* Default to Light Theme */
            --bg-color: var(--bg-light);
            --bg-gradient: var(--bg-gradient-light);
            --text-color: var(--text-color-light);
            --glass-bg: var(--glass-bg-light);
            --glass-border: var(--glass-border-light);
            --glow-color: var(--glow-light);
            --shadow-color: var(--shadow-light);
        }

        .dark-theme {
            --bg-color: var(--bg-dark);
            --bg-gradient: var(--bg-gradient-dark);
            --text-color: var(--text-color-dark);
            --glass-bg: var(--glass-bg-dark);
            --glass-border: var(--glass-border-dark);
            --glow-color: var(--glow-dark);
            --shadow-color: var(--shadow-dark);
        }

        *, *::before, *::after {
            box-sizing: border-box;
            margin: 0;
            padding: 0;
        }

        body {
            font-family: var(--font-family);
            background-color: var(--bg-color);
            background-image: var(--bg-gradient);
            color: var(--text-color);
            padding: 2rem;
            transition: background 0.4s ease, color 0.4s ease;
        }
        
        h1, h2, h3 {
             margin-bottom: 1rem;
             text-shadow: 0 1px 2px var(--shadow-color);
        }

        h1 { font-size: 2.5rem; text-align: center; }
        h2 { font-size: 1.8rem; border-bottom: 1px solid var(--glass-border); padding-bottom: 0.5rem; margin-top: 2rem; }
        h3 { font-size: 1.2rem; opacity: 0.8; }
        
        .showcase-grid {
            display: grid;
            grid-template-columns: repeat(auto-fit, minmax(350px, 1fr));
            gap: 2rem;
        }

        .showcase-card {
            background: var(--glass-bg);
            backdrop-filter: blur(25px);
            -webkit-backdrop-filter: blur(25px);
            border-radius: 16px;
            border: 1px solid var(--glass-border);
            padding: 1.5rem;
            box-shadow: 0 8px 32px 0 var(--shadow-color);
            display: flex;
            flex-direction: column;
            gap: 1.5rem;
        }
        
        /* Helper for alignment */
        .flex-center { display: flex; align-items: center; justify-content: center; gap: 1rem; flex-wrap: wrap; }


        /* ------------------------- */
        /* --- COMPONENTS --- */
        /* ------------------------- */

        /* --- Theme Switcher (Custom for this page) --- */
        .theme-switcher {
            position: fixed;
            top: 20px;
            right: 20px;
            z-index: 1000;
        }

        /* --- Accordion --- */
        .accordion .accordion-item {
            background: var(--glass-bg);
            border: 1px solid var(--glass-border);
            border-radius: 12px;
            overflow: hidden;
            transition: all 0.4s ease;
        }
        .accordion .accordion-header {
            display: flex;
            justify-content: space-between;
            align-items: center;
            padding: 1rem;
            cursor: pointer;
            transition: background 0.3s ease;
        }
        .accordion .accordion-header:hover { background: rgba(255, 255, 255, 0.1); }
        .accordion .accordion-chevron {
            transition: transform 0.4s cubic-bezier(0.23, 1, 0.32, 1);
        }
        .accordion .accordion-item.active .accordion-chevron { transform: rotate(90deg); }
        .accordion .accordion-content {
            max-height: 0;
            overflow: hidden;
            transition: max-height 0.4s cubic-bezier(0.23, 1, 0.32, 1), padding 0.4s ease;
            padding: 0 1rem;
        }
        .accordion .accordion-item.active .accordion-content {
            max-height: 200px;
            padding: 0 1rem 1rem 1rem;
        }

        /* --- Alert --- */
        .alert {
            padding: 1rem;
            border-radius: 12px;
            border: 1px solid var(--glass-border);
            backdrop-filter: blur(15px);
            display: flex;
            align-items: center;
            gap: 1rem;
        }
        .alert-info { background: rgba(52, 152, 219, 0.15); border-left: 4px solid #3498db; }
        .alert-success { background: rgba(46, 204, 113, 0.15); border-left: 4px solid #2ecc71; }
        .alert-danger { background: rgba(231, 76, 60, 0.15); border-left: 4px solid #e74c3c; }
        .alert button { background: none; border: none; color: var(--text-color); opacity: 0.7; cursor: pointer; margin-left: auto;}

        /* --- Avatar & User --- */
        .avatar, .user { display: inline-flex; align-items: center; gap: 0.75rem; }
        .avatar-frame {
            position: relative;
            background: var(--glass-bg);
            backdrop-filter: blur(10px);
            border-radius: 50%;
            padding: 4px;
            transition: all 0.3s ease;
        }
        .avatar-frame:hover { transform: translateY(-2px); box-shadow: 0 4px 15px var(--shadow-color); }
        .avatar-img { width: 48px; height: 48px; border-radius: 50%; display: block; }
        .avatar-status {
            position: absolute;
            bottom: 4px; right: 4px;
            width: 12px; height: 12px;
            border-radius: 50%;
            border: 2px solid var(--bg-color);
        }
        .avatar-status.online { background-color: #2ecc71; }
        .avatar-status.offline { background-color: #95a5a6; }
        .user-info .name { font-weight: 600; }
        .user-info .handle { font-size: 0.9em; opacity: 0.7; }

        /* --- Badge --- */
        .badge {
            display: inline-block;
            padding: 0.25em 0.6em;
            font-size: 0.75rem;
            font-weight: 700;
            line-height: 1;
            text-align: center;
            white-space: nowrap;
            vertical-align: baseline;
            border-radius: 20px;
            backdrop-filter: blur(5px);
            color: white;
            text-shadow: 0 0 5px rgba(0,0,0,0.5);
        }
        .badge-danger { background: rgba(220, 53, 69, 0.5); }
        .badge-primary { background: rgba(0, 122, 255, 0.5); }
        .badge-success { background: rgba(40, 167, 69, 0.5); }

        /* --- Breadcrumbs --- */
        .breadcrumbs ol { list-style: none; display: flex; gap: 0.5rem; align-items: center; }
        .breadcrumbs .breadcrumb-item a { color: var(--text-color); opacity: 0.7; text-decoration: none; transition: opacity 0.3s ease; }
        .breadcrumbs .breadcrumb-item a:hover { opacity: 1; }
        .breadcrumbs .breadcrumb-item.active { opacity: 1; font-weight: 600; }
        .breadcrumbs .breadcrumb-separator { opacity: 0.4; }

        /* --- Button --- */
        .btn {
            padding: 0.75rem 1.5rem;
            border-radius: 10px;
            border: 1px solid var(--glass-border);
            background: var(--glass-bg);
            backdrop-filter: blur(12px);
            color: var(--text-color);
            cursor: pointer;
            font-size: 1rem;
            font-weight: 600;
            position: relative;
            overflow: hidden;
            transition: transform 0.3s ease, box-shadow 0.3s ease, background 0.3s ease;
        }
        .btn:hover {
            transform: translateY(-3px);
            box-shadow: 0 8px 20px var(--shadow-color);
            background: rgba(255, 255, 255, 0.1);
        }
        .btn:active { transform: translateY(-1px); }
        .btn-primary { background: linear-gradient(135deg, rgba(0, 122, 255, 0.3), rgba(88, 86, 214, 0.3)); }
        .btn-primary:hover { background: linear-gradient(135deg, rgba(0, 122, 255, 0.4), rgba(88, 86, 214, 0.4)); }
        
        /* --- Card --- */
        /* See .showcase-card for primary style */

        /* --- Checkbox & Radio --- */
        .form-check {
            display: flex;
            align-items: center;
            gap: 0.75rem;
            cursor: pointer;
        }
        .form-check-input {
            appearance: none;
            width: 20px; height: 20px;
            border: 2px solid var(--glass-border);
            background: var(--glass-bg);
            border-radius: 6px;
            transition: all 0.3s ease;
            position: relative;
            display: grid;
            place-content: center;
        }
        .form-check-input[type="radio"] { border-radius: 50%; }
        .form-check-input::before {
            content: '';
            width: 10px; height: 10px;
            transform: scale(0);
            transition: 120ms transform ease-in-out;
            box-shadow: inset 1em 1em var(--glow-color);
            background-color: var(--glow-color);
        }
        .form-check-input[type="checkbox"]::before { clip-path: polygon(14% 44%, 0 65%, 50% 100%, 100% 16%, 80% 0%, 43% 62%); }
        .form-check-input[type="radio"]::before { border-radius: 50%; }
        .form-check-input:checked {
            border-color: var(--glow-color);
            box-shadow: 0 0 10px var(--glow-color);
        }
        .form-check-input:checked::before { transform: scale(1); }

        /* --- Chip --- */
        .chip {
            display: inline-flex; align-items: center; gap: 0.5rem;
            padding: 4px 10px;
            background: var(--glass-bg);
            backdrop-filter: blur(10px);
            border: 1px solid var(--glass-border);
            border-radius: 20px;
            font-size: 0.9em;
            transition: all 0.3s ease;
        }
        .chip:hover { transform: translateY(-2px); box-shadow: 0 4px 10px var(--shadow-color); }
        .chip .chip-close { background:none; border:none; color:var(--text-color); opacity:0.6; cursor:pointer; font-size: 1.2em; line-height: 1; }
        
        /* --- Progress & Spinner --- */
        .progress {
            width: 100%; height: 10px;
            background: var(--glass-bg);
            border-radius: 10px;
            overflow: hidden;
            border: 1px solid var(--glass-border);
        }
        .progress-bar {
            height: 100%;
            background: linear-gradient(90deg, #3498db, #8e44ad);
            box-shadow: 0 0 15px #3498db;
            border-radius: 10px;
            transition: width 0.5s ease;
            position: relative;
            overflow: hidden;
        }
        .progress-bar::after {
             content: ''; position: absolute; top: 0; left: 0; right: 0; bottom: 0;
             background: linear-gradient(90deg, transparent, rgba(255,255,255,0.3), transparent);
             animation: shimmer 2s infinite linear;
        }
        @keyframes shimmer { 0% { transform: translateX(-100%); } 100% { transform: translateX(100%); } }
        
        .spinner {
            width: 40px; height: 40px;
            border: 4px solid var(--glass-bg);
            border-top-color: var(--text-color);
            border-radius: 50%;
            animation: spin 1s linear infinite;
        }
        @keyframes spin { 100% { transform: rotate(360deg); } }
        
        /* --- Code & Snippet --- */
        .code-block, .snippet {
            background: rgba(0, 0, 0, 0.4);
            backdrop-filter: blur(25px);
            border-radius: 8px;
            padding: 1rem;
            font-family: 'SF Mono', 'Fira Code', monospace;
            color: #f8f8f2;
            border: 1px solid var(--glass-border);
        }
        .snippet { display: inline-block; padding: 0.2rem 0.5rem; }
        .code-block pre { white-space: pre-wrap; }

        /* --- Divider --- */
        .divider {
            height: 1px;
            width: 100%;
            background: var(--glass-border);
            box-shadow: 0 0 10px rgba(255, 255, 255, 0.1);
        }

        /* --- Drawer --- */
        .drawer-container {
            position: fixed;
            top: 0; left: 0;
            width: 100%; height: 100%;
            z-index: 1001;
            pointer-events: none;
            transition: background 0.4s ease;
        }
        .drawer-container.active {
            pointer-events: all;
            background: rgba(0,0,0,0.3);
        }
        .drawer {
            position: fixed;
            top: 0; right: 0;
            height: 100%;
            width: 350px;
            background: var(--glass-bg);
            backdrop-filter: blur(40px);
            box-shadow: -10px 0 30px var(--shadow-color);
            padding: 2rem;
            transform: translateX(100%);
            transition: transform 0.4s cubic-bezier(0.23, 1, 0.32, 1);
        }
        .drawer-container.active .drawer {
            transform: translateX(0);
        }

        /* --- Form & Input --- */
        .form-group { display: flex; flex-direction: column; gap: 0.5rem; }
        .input, .textarea {
            width: 100%;
            padding: 0.75rem 1rem;
            background: rgba(0,0,0,0.1); /* Slightly recessed look */
            border: 1px solid var(--glass-border);
            border-radius: 8px;
            font-size: 1rem;
            color: var(--text-color);
            transition: all 0.3s ease;
        }
        .input:focus, .textarea:focus {
            outline: none;
            border-color: var(--glow-color);
            box-shadow: 0 0 15px var(--glow-color);
        }
        .textarea { min-height: 100px; resize: vertical; }

        /* --- OTP Input --- */
        .otp-group { display: flex; gap: 10px; justify-content: center; }
        .otp-input {
            width: 45px; height: 50px;
            text-align: center; font-size: 1.5rem;
            background: rgba(0,0,0,0.1);
            border: 1px solid var(--glass-border);
            border-radius: 8px;
            color: var(--text-color);
            transition: all 0.3s ease;
        }
        .otp-input:focus {
            transform: scale(1.1);
            border-color: var(--glow-color);
            box-shadow: 0 0 15px var(--glow-color);
        }

        /* --- Image --- */
        .image-frame {
            border-radius: 12px;
            padding: 8px;
            background: var(--glass-bg);
            border: 1px solid var(--glass-border);
            transition: all 0.3s ease;
            display: inline-block;
        }
        .image-frame:hover { box-shadow: 0 0 20px var(--shadow-color); }
        .image-frame img { display: block; border-radius: 8px; max-width: 100%; }

        /* --- Keyboard Key --- */
        .kbd-key {
            display: inline-block;
            padding: 0.3rem 0.7rem;
            background: var(--glass-bg);
            border: 1px solid var(--glass-border);
            border-radius: 6px;
            box-shadow: 0 2px 0 var(--glass-border);
            font-family: var(--font-family);
            font-weight: 600;
            transition: all 0.1s ease-in-out;
        }
        .kbd-key:active { transform: translateY(1px); box-shadow: 0 1px 0 var(--glass-border); }

        /* --- Link --- */
        .link {
            text-decoration: none;
            font-weight: 600;
            position: relative;
            background: linear-gradient(120deg, #A0C4FF, #BDB2FF);
            -webkit-background-clip: text;
            -webkit-text-fill-color: transparent;
            transition: filter 0.3s ease;
        }
        .dark-theme .link { background: linear-gradient(120deg, #81e6d9, #d53f8c); -webkit-background-clip: text; }
        .link:hover { filter: brightness(1.5); }
        .link::after {
            content: '';
            position: absolute;
            width: 100%;
            height: 1px;
            bottom: -2px; left: 0;
            background-color: var(--glow-color);
            transform: scaleX(0);
            transform-origin: bottom right;
            transition: transform 0.3s ease-out;
        }
        .link:hover::after { transform: scaleX(1); transform-origin: bottom left; }
        
        /* --- Modal --- */
        .modal-container {
            position: fixed; top: 0; left: 0; width: 100%; height: 100%;
            display: grid; place-items: center;
            z-index: 1002;
            visibility: hidden; opacity: 0;
            transition: visibility 0.3s, opacity 0.3s;
        }
        .modal-container.active { visibility: visible; opacity: 1; }
        .modal-overlay {
            position: absolute; top: 0; left: 0; width: 100%; height: 100%;
            background: rgba(0,0,0,0.3);
            backdrop-filter: blur(10px);
        }
        .modal-content {
            position: relative; z-index: 1;
            width: 90%; max-width: 500px;
            background: var(--glass-bg);
            backdrop-filter: blur(40px);
            border: 1px solid var(--glass-border);
            border-radius: 20px;
            padding: 2rem;
            transform: scale(0.9);
            transition: transform 0.3s cubic-bezier(0.23, 1, 0.32, 1);
        }
        .modal-container.active .modal-content { transform: scale(1); }
        .modal-header { display: flex; justify-content: space-between; align-items: center; }

        /* --- Navbar --- */
        .navbar {
            position: fixed; top: 0; left: 0; right: 0;
            z-index: 100;
            padding: 1rem 2rem;
            background: var(--glass-bg);
            backdrop-filter: blur(30px);
            border-bottom: 1px solid var(--glass-border);
            display: flex;
            justify-content: space-between;
            align-items: center;
            transition: background 0.3s ease;
        }
        .navbar-brand { font-weight: 700; font-size: 1.2rem; }
        .navbar-links { display: flex; gap: 1.5rem; }

        /* --- Pagination --- */
        .pagination { display: flex; gap: 0.5rem; align-items: center; }
        .pagination a {
            display: grid; place-content: center;
            width: 36px; height: 36px;
            border-radius: 50%;
            background: var(--glass-bg);
            border: 1px solid var(--glass-border);
            text-decoration: none; color: var(--text-color);
            transition: all 0.3s ease;
        }
        .pagination a:hover { transform: translateY(-2px); box-shadow: 0 4px 10px var(--shadow-color); }
        .pagination a.active {
            background: var(--glow-color);
            color: white;
            box-shadow: 0 0 15px var(--glow-color);
            transform: scale(1.1);
        }
        .pagination .ellipsis { padding: 0 0.5rem; }

        /* --- Popover & Tooltip --- */
        .has-popover, .has-tooltip { position: relative; display: inline-block; }
        .popover, .tooltip {
            position: absolute;
            bottom: 125%;
            left: 50%;
            transform: translateX(-50%);
            padding: 0.75rem;
            border-radius: 8px;
            background: rgba(20,20,20,0.7);
            backdrop-filter: blur(15px);
            border: 1px solid var(--glass-border);
            color: #fff;
            box-shadow: 0 4px 20px var(--shadow-color);
            z-index: 10;
            width: max-content;
            max-width: 250px;
            visibility: hidden;
            opacity: 0;
            transition: opacity 0.3s, visibility 0.3s, transform 0.3s;
        }
        .popover { padding: 1rem; }
        .has-popover:hover .popover, .has-tooltip:hover .tooltip {
            visibility: visible;
            opacity: 1;
            transform: translateX(-50%) translateY(-10px);
        }

        /* --- Skeleton --- */
        .skeleton {
            background: var(--glass-bg);
            border-radius: 4px;
            position: relative;
            overflow: hidden;
        }
        .skeleton::after {
             content: ''; position: absolute; top: 0; left: 0; right: 0; bottom: 0;
             background: linear-gradient(90deg, transparent, rgba(255,255,255,0.1), transparent);
             animation: shimmer 1.5s infinite;
        }
        .sk-avatar { width: 48px; height: 48px; border-radius: 50%; }
        .sk-line { height: 1em; margin-bottom: 0.5em; }
        .sk-line:last-child { margin-bottom: 0; }

        /* --- Slider --- */
        .slider-container { display: flex; align-items: center; gap: 1rem; }
        .slider {
            -webkit-appearance: none;
            width: 100%;
            height: 8px;
            background: var(--glass-bg);
            border: 1px solid var(--glass-border);
            border-radius: 5px;
            outline: none;
        }
        .slider::-webkit-slider-thumb {
            -webkit-appearance: none;
            appearance: none;
            width: 20px;
            height: 20px;
            background: white;
            border-radius: 50%;
            cursor: pointer;
            box-shadow: 0 0 15px rgba(255,255,255,0.5);
            transition: box-shadow 0.3s ease;
        }
        .slider:hover::-webkit-slider-thumb { box-shadow: 0 0 20px var(--glow-color); }
        .slider-value { font-weight: 600; min-width: 30px; text-align: center; }

        /* --- Switch --- */
        .switch {
            position: relative;
            display: inline-block;
            width: 50px;
            height: 28px;
        }
        .switch input { opacity: 0; width: 0; height: 0; }
        .switch-slider {
            position: absolute; cursor: pointer;
            top: 0; left: 0; right: 0; bottom: 0;
            background-color: var(--glass-bg);
            border: 1px solid var(--glass-border);
            border-radius: 28px;
            transition: all 0.4s;
        }
        .switch-slider:before {
            position: absolute;
            content: "";
            height: 20px; width: 20px;
            left: 3px; bottom: 3px;
            background-color: white;
            border-radius: 50%;
            box-shadow: 0 2px 8px var(--shadow-color);
            transition: all 0.4s cubic-bezier(0.23, 1, 0.32, 1);
        }
        .switch input:checked + .switch-slider {
            background-color: var(--glow-color);
            box-shadow: 0 0 10px var(--glow-color);
        }
        .switch input:checked + .switch-slider:before {
            transform: translateX(22px);
        }

        /* --- Table --- */
        .table-container {
            border: 1px solid var(--glass-border);
            border-radius: 12px;
            overflow: hidden;
            background: var(--glass-bg);
        }
        .table {
            width: 100%;
            border-collapse: collapse;
        }
        .table th, .table td {
            padding: 1rem;
            text-align: left;
        }
        .table thead {
            backdrop-filter: blur(10px);
            background: rgba(0,0,0,0.1);
        }
        .table tbody tr {
            transition: background 0.3s ease;
            border-bottom: 1px solid var(--glass-border);
        }
        .table tbody tr:last-child { border-bottom: none; }
        .table tbody tr:hover { background: rgba(255,255,255,0.1); }
        
        /* --- Tabs --- */
        .tabs { position: relative; border-bottom: 1px solid var(--glass-border); }
        .tab-list { list-style: none; display: flex; gap: 1.5rem; }
        .tab-item {
            padding: 1rem 0.5rem;
            cursor: pointer;
            color: var(--text-color);
            opacity: 0.7;
            transition: opacity 0.3s ease;
        }
        .tab-item.active, .tab-item:hover { opacity: 1; }
        .tab-indicator {
            position: absolute;
            bottom: -1px; /* To overlap the border */
            height: 2px;
            background-color: var(--glow-color);
            box-shadow: 0 0 10px var(--glow-color);
            transition: all 0.4s cubic-bezier(0.23, 1, 0.32, 1);
        }
        .tab-content { padding-top: 1rem; }
        .tab-panel { display: none; }
        .tab-panel.active { display: block; }
        
        /* --- Dropdown, Listbox, etc. --- */
        .dropdown { position: relative; display: inline-block; }
        .dropdown-menu, .listbox {
            position: absolute;
            top: 110%;
            left: 0;
            z-index: 100;
            min-width: 180px;
            padding: 8px;
            background: var(--glass-bg);
            backdrop-filter: blur(25px);
            border: 1px solid var(--glass-border);
            border-radius: 10px;
            box-shadow: 0 8px 32px var(--shadow-color);
            visibility: hidden; opacity: 0;
            transform: translateY(-10px);
            transition: all 0.3s ease;
        }
        .dropdown.active .dropdown-menu { visibility: visible; opacity: 1; transform: translateY(0); }
        .dropdown-item, .listbox-item {
            padding: 0.75rem 1rem;
            border-radius: 6px;
            cursor: pointer;
            transition: background 0.2s ease;
        }
        .dropdown-item:hover, .listbox-item:hover { background: rgba(255, 255, 255, 0.1); }
        .listbox-item[aria-selected="true"] { background: var(--glow-color); color: #fff; }

    </style>
</head>
<body>

    <!-- NAVBAR -->
    <nav class="navbar">
        <div class="navbar-brand">Liquid Glass UI</div>
        <div class="navbar-links">
            <div class="link">Home</div>
            <div class="link">Components</div>
            <div class="link">About</div>
        </div>
        <div class="theme-switcher">
            <label class="switch">
                <input type="checkbox" id="theme-toggle-checkbox">
                <span class="switch-slider"></span>
            </label>
        </div>
    </nav>
    
    <div style="height: 80px;"></div> <!-- Spacer for fixed navbar -->

    <h1>Liquid Glass UI Component Showcase</h1>

    <div class="showcase-grid">

        <!-- Buttons, Switch, Chips -->
        <div class="showcase-card">
            <h2>Buttons & Interactive</h2>
            <h3>Buttons</h3>
            <div class="flex-center">
                <button class="btn">Standard</button>
                <button class="btn btn-primary">Primary Action</button>
            </div>
            <h3>Switch</h3>
            <div class="flex-center">
                <label class="switch"><input type="checkbox" checked><span class="switch-slider"></span></label>
            </div>
            <h3>Chips</h3>
            <div class="flex-center">
                <div class="chip">Category 1</div>
                <div class="chip">Removable <button class="chip-close">×</button></div>
            </div>
            <h3>Keyboard Key</h3>
            <div class="flex-center">
                <span class="kbd-key">Ctrl</span> + <span class="kbd-key">K</span>
            </div>
        </div>
        
        <!-- Navigation -->
        <div class="showcase-card">
            <h2>Navigation</h2>
            <h3>Tabs</h3>
            <div class="tabs-container">
                <div class="tabs">
                    <ul class="tab-list">
                        <li class="tab-item active" data-tab="1">Profile</li>
                        <li class="tab-item" data-tab="2">Dashboard</li>
                        <li class="tab-item" data-tab="3">Settings</li>
                    </ul>
                    <div class="tab-indicator"></div>
                </div>
                <div class="tab-content">
                    <div class="tab-panel active" id="tab-panel-1">Content for Profile tab.</div>
                    <div class="tab-panel" id="tab-panel-2">Content for Dashboard tab.</div>
                    <div class="tab-panel" id="tab-panel-3">Content for Settings tab.</div>
                </div>
            </div>
            <h3>Breadcrumbs</h3>
            <nav class="breadcrumbs">
                <ol>
                    <li class="breadcrumb-item"><a href="#">Home</a></li>
                    <li class="breadcrumb-separator">/</li>
                    <li class="breadcrumb-item"><a href="#">Products</a></li>
                    <li class="breadcrumb-separator">/</li>
                    <li class="breadcrumb-item active">Laptops</li>
                </ol>
            </nav>
            <h3>Pagination</h3>
            <nav class="pagination flex-center">
                <a href="#">«</a>
                <a href="#">1</a>
                <a href="#" class="active">2</a>
                <a href="#">3</a>
                <span class="ellipsis">...</span>
                <a href="#">10</a>
                <a href="#">»</a>
            </nav>
            <h3>Link</h3>
            <div class="flex-center">
                This is a <a href="#" class="link">gorgeous link</a>.
            </div>
        </div>
        
        <!-- Form Elements -->
        <div class="showcase-card">
            <h2>Form Elements</h2>
            <div class="form-group">
                <label for="name">Text Input</label>
                <input type="text" id="name" class="input" placeholder="Enter your name">
            </div>
             <div class="form-group">
                <label for="num">Number Input</label>
                <input type="number" id="num" class="input" placeholder="123">
            </div>
            <div class="form-group">
                <label for="date">Date Input</label>
                <input type="date" id="date" class="input">
            </div>
            <div class="form-group">
                <label for="time">Time Input</label>
                <input type="time" id="time" class="input">
            </div>
            <div class="form-group">
                <label for="comments">Text Area</label>
                <textarea id="comments" class="textarea" placeholder="Leave a comment..."></textarea>
            </div>
            <div class="form-group">
                <h3>Checkbox Group</h3>
                <label class="form-check"><input type="checkbox" class="form-check-input" checked> Option 1</label>
                <label class="form-check"><input type="checkbox" class="form-check-input"> Option 2</label>
            </div>
            <div class="form-group">
                <h3>Radio Group</h3>
                <label class="form-check"><input type="radio" name="radio-group" class="form-check-input" checked> Select A</label>
                <label class="form-check"><input type="radio" name="radio-group" class="form-check-input"> Select B</label>
            </div>
        </div>
        
        <!-- Complex Inputs -->
        <div class="showcase-card">
             <h2>Complex Inputs</h2>
             <h3>Dropdown</h3>
             <div class="dropdown" id="myDropdown">
                 <button class="btn">Dropdown Menu</button>
                 <div class="dropdown-menu">
                     <div class="dropdown-item">Action</div>
                     <div class="dropdown-item">Another action</div>
                     <div class="dropdown-item">Something else here</div>
                 </div>
             </div>
             <h3>Slider</h3>
             <div class="slider-container">
                <input type="range" min="1" max="100" value="50" class="slider" id="mySlider">
                <span class="slider-value" id="sliderValue">50</span>
             </div>
             <h3>Input OTP</h3>
             <div class="otp-group">
                 <input type="text" class="otp-input" maxlength="1">
                 <input type="text" class="otp-input" maxlength="1">
                 <input type="text" class="otp-input" maxlength="1">
                 <input type="text" class="otp-input" maxlength="1">
             </div>
        </div>
        
        <!-- User & Data Display -->
        <div class="showcase-card">
            <h2>User & Data Display</h2>
            <h3>Avatar</h3>
            <div class="flex-center">
                <div class="avatar">
                    <div class="avatar-frame">
                        <img src="https://i.pravatar.cc/48?u=a" alt="Avatar" class="avatar-img">
                        <div class="avatar-status online"></div>
                    </div>
                </div>
                <div class="avatar">
                    <div class="avatar-frame">
                        <img src="https://i.pravatar.cc/48?u=b" alt="Avatar" class="avatar-img">
                        <div class="avatar-status offline"></div>
                    </div>
                </div>
            </div>
            <h3>User Component</h3>
            <div class="user">
                <div class="avatar-frame">
                    <img src="https://i.pravatar.cc/48?u=c" alt="User Avatar" class="avatar-img">
                </div>
                <div class="user-info">
                    <div class="name">Ada Lovelace</div>
                    <div class="handle">@ada</div>
                </div>
            </div>
            <h3>Badges</h3>
            <div class="flex-center">
                <span class="badge badge-primary">New</span>
                <span class="badge badge-success">Active</span>
                <span class="badge badge-danger">99+</span>
            </div>
        </div>

        <!-- Feedback & Status -->
        <div class="showcase-card">
            <h2>Feedback & Status</h2>
            <h3>Alerts</h3>
            <div class="alert alert-info">
                This is an informational alert.
                <button class="alert-dismiss">×</button>
            </div>
            <div class="alert alert-success">
                Your profile was updated successfully!
                <button class="alert-dismiss">×</button>
            </div>
            <div class="alert alert-danger">
                Failed to upload file.
                <button class="alert-dismiss">×</button>
            </div>
            <h3>Progress Bars</h3>
            <div class="progress"><div class="progress-bar" style="width: 75%;"></div></div>
            <h3>Spinner & Circular Progress</h3>
            <div class="flex-center">
                <div class="spinner"></div>
            </div>
            <h3>Skeleton Loader</h3>
            <div class="flex-center" style="width: 100%; align-items: flex-start;">
                <div class="skeleton sk-avatar"></div>
                <div style="flex: 1;">
                    <div class="skeleton sk-line" style="width: 60%;"></div>
                    <div class="skeleton sk-line" style="width: 90%;"></div>
                    <div class="skeleton sk-line" style="width: 80%;"></div>
                </div>
            </div>
        </div>

        <!-- Containers & Popups -->
        <div class="showcase-card">
            <h2>Containers & Popups</h2>
            <h3>Modal</h3>
            <button class="btn" id="openModalBtn">Open Modal</button>
            <h3>Drawer</h3>
            <button class="btn" id="openDrawerBtn">Open Drawer</button>
            <h3>Popover & Tooltip</h3>
            <div class="flex-center">
                <div class="has-tooltip">
                    <span class="btn">Hover for Tooltip</span>
                    <div class="tooltip">Just a simple tip.</div>
                </div>
                <div class="has-popover">
                    <span class="btn">Hover for Popover</span>
                    <div class="popover">
                        <h4>Rich Content</h4>
                        <p>Popovers can contain more complex HTML elements.</p>
                    </div>
                </div>
            </div>
        </div>

        <!-- Content & Structure -->
        <div class="showcase-card">
            <h2>Content & Structure</h2>
            <h3>Accordion</h3>
            <div class="accordion">
                <div class="accordion-item">
                    <div class="accordion-header">
                        <span>First Item</span>
                        <svg class="accordion-chevron" width="24" height="24" viewBox="0 0 24 24" fill="none" stroke="currentColor" stroke-width="2" stroke-linecap="round" stroke-linejoin="round"><polyline points="9 18 15 12 9 6"></polyline></svg>
                    </div>
                    <div class="accordion-content">
                        This is the content of the first accordion item. It's hidden by default.
                    </div>
                </div>
                <div class="accordion-item">
                    <div class="accordion-header">
                        <span>Second Item</span>
                        <svg class="accordion-chevron" width="24" height="24" viewBox="0 0 24 24" fill="none" stroke="currentColor" stroke-width="2" stroke-linecap="round" stroke-linejoin="round"><polyline points="9 18 15 12 9 6"></polyline></svg>
                    </div>
                    <div class="accordion-content">
                        This is the content of the second accordion item.
                    </div>
                </div>
            </div>
            <h3>Image</h3>
            <div class="image-frame">
                <img src="https://picsum.photos/400/200" alt="Placeholder Image">
            </div>
            <h3>Code & Snippet</h3>
            <p>This is an inline <code class="snippet">const a = 1;</code> snippet.</p>
            <div class="code-block">
                <pre><code>function greet() {
  console.log("Hello, Liquid World!");
}</code></pre>
            </div>
            <h3>Divider & Spacer</h3>
            <p>Content above the divider.</p>
            <div class="divider"></div>
            <!-- Spacer is invisible but you would use a div with margin/height -->
            <p>Content below the divider.</p>
        </div>
        
        <!-- Table -->
        <div class="showcase-card" style="grid-column: 1 / -1;">
            <h2>Table</h2>
            <div class="table-container">
                <table class="table">
                    <thead>
                        <tr>
                            <th>User</th>
                            <th>Status</th>
                            <th>Role</th>
                            <th>Last Login</th>
                        </tr>
                    </thead>
                    <tbody>
                        <tr>
                            <td><div class="user"><div class="avatar-frame"><img src="https://i.pravatar.cc/48?u=d" class="avatar-img"></div><div>Alex Ray</div></div></td>
                            <td><span class="badge badge-success">Active</span></td>
                            <td>Admin</td>
                            <td>2 hours ago</td>
                        </tr>
                        <tr>
                            <td><div class="user"><div class="avatar-frame"><img src="https://i.pravatar.cc/48?u=e" class="avatar-img"></div><div>Kate Winslet</div></div></td>
                            <td><span class="badge badge-primary">Pending</span></td>
                            <td>Editor</td>
                            <td>1 day ago</td>
                        </tr>
                        <tr>
                            <td><div class="user"><div class="avatar-frame"><img src="https://i.pravatar.cc/48?u=f" class="avatar-img"></div><div>John Doe</div></div></td>
                            <td><span class="badge badge-danger">Banned</span></td>
                            <td>Member</td>
                            <td>1 week ago</td>
                        </tr>
                    </tbody>
                </table>
            </div>
        </div>

    </div>

    <!-- Modal HTML -->
    <div class="modal-container" id="myModal">
        <div class="modal-overlay"></div>
        <div class="modal-content">
            <div class="modal-header">
                <h2>Modal Title</h2>
                <button class="btn" id="closeModalBtn">×</button>
            </div>
            <p>This is the content of the modal. It floats above everything else and demands attention. You can close it by clicking the button or the overlay.</p>
        </div>
    </div>
    
    <!-- Drawer HTML -->
    <div class="drawer-container" id="myDrawer">
        <div class="drawer">
            <h2>Drawer Panel</h2>
            <p>This panel slides in from the side. It's great for supplementary content or navigation.</p>
            <button class="btn" id="closeDrawerBtn">Close</button>
        </div>
    </div>


<script>
document.addEventListener('DOMContentLoaded', function() {

    // --- Theme Switcher ---
    const themeToggle = document.getElementById('theme-toggle-checkbox');
    themeToggle.addEventListener('change', function() {
        document.body.classList.toggle('dark-theme', this.checked);
    });

    // --- Accordion ---
    document.querySelectorAll('.accordion .accordion-header').forEach(header => {
        header.addEventListener('click', () => {
            header.parentElement.classList.toggle('active');
        });
    });

    // --- Alert Dismiss ---
    document.querySelectorAll('.alert-dismiss').forEach(button => {
        button.addEventListener('click', (e) => {
            e.target.closest('.alert').style.display = 'none';
        });
    });
    
    // --- Tabs ---
    const tabsContainer = document.querySelector('.tabs-container');
    if(tabsContainer) {
        const tabList = tabsContainer.querySelector('.tab-list');
        const tabItems = tabsContainer.querySelectorAll('.tab-item');
        const tabIndicator = tabsContainer.querySelector('.tab-indicator');
        const tabPanels = tabsContainer.querySelectorAll('.tab-panel');

        function moveIndicator(el) {
            tabIndicator.style.width = `${el.offsetWidth}px`;
            tabIndicator.style.left = `${el.offsetLeft}px`;
        }

        moveIndicator(tabList.querySelector('.active'));

        tabList.addEventListener('click', (e) => {
            const targetTab = e.target.closest('.tab-item');
            if (!targetTab) return;
            
            tabItems.forEach(tab => tab.classList.remove('active'));
            targetTab.classList.add('active');
            moveIndicator(targetTab);
            
            tabPanels.forEach(panel => panel.classList.remove('active'));
            document.getElementById(`tab-panel-${targetTab.dataset.tab}`).classList.add('active');
        });
    }

    // --- Modal ---
    const modal = document.getElementById('myModal');
    const openModalBtn = document.getElementById('openModalBtn');
    const closeModalBtn = document.getElementById('closeModalBtn');
    if(modal) {
        openModalBtn.addEventListener('click', () => modal.classList.add('active'));
        closeModalBtn.addEventListener('click', () => modal.classList.remove('active'));
        modal.querySelector('.modal-overlay').addEventListener('click', () => modal.classList.remove('active'));
    }

    // --- Drawer ---
    const drawer = document.getElementById('myDrawer');
    const openDrawerBtn = document.getElementById('openDrawerBtn');
    const closeDrawerBtn = document.getElementById('closeDrawerBtn');
    if(drawer) {
        openDrawerBtn.addEventListener('click', () => drawer.classList.add('active'));
        closeDrawerBtn.addEventListener('click', () => drawer.classList.remove('active'));
        drawer.addEventListener('click', (e) => {
            if (e.target === drawer) { // Click on the overlay part
                 drawer.classList.remove('active');
            }
        });
    }

    // --- Slider ---
    const slider = document.getElementById('mySlider');
    const sliderValue = document.getElementById('sliderValue');
    if(slider) {
        slider.addEventListener('input', (e) => {
            sliderValue.textContent = e.target.value;
        });
    }

    // --- Dropdown ---
    const dropdown = document.getElementById('myDropdown');
    if(dropdown) {
        dropdown.querySelector('.btn').addEventListener('click', () => {
            dropdown.classList.toggle('active');
        });
        // Close dropdown when clicking outside
        document.addEventListener('click', (e) => {
            if (!dropdown.contains(e.target)) {
                dropdown.classList.remove('active');
            }
        });
    }

    // --- OTP Input auto-focus ---
    const otpInputs = document.querySelectorAll('.otp-input');
    otpInputs.forEach((input, index) => {
        input.addEventListener('keyup', (e) => {
            if (e.key >= 0 && e.key <= 9 && index < otpInputs.length - 1) {
                otpInputs[index + 1].focus();
            } else if (e.key === 'Backspace' && index > 0) {
                otpInputs[index - 1].focus();
            }
        });
    });

});
</script>

</body>
</html>
```
