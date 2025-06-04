# Interactive Timeline CV

This project is a single-page HTML application that displays a personal CV or timeline of experiences in an interactive and visually appealing way.

[![View Demo](https://img.shields.io/badge/View-Demo-green?style=for-the-badge)](https://ismntr.github.io/cv/)
## Features

*   **Dynamic Timeline:** Displays events (education, work experience, certifications, etc.) along a vertical timeline.
*   **Categorized & Color-Coded Items:** Each experience is categorized (e.g., "Eğitim", "İş", "Staj") and color-coded for easy differentiation.
*   **Detailed Information Cards:** Each event on the timeline has an associated card showing details like repository name, label, duration, description, and sub-branches/skills.
*   **Draggable Cards:** The information cards can be dragged and dropped around the timeline area.
*   **SVG Connectors:** Lines dynamically connect the timeline nodes to their respective information cards, updating as cards are moved.
*   **Responsive Design:** The layout adapts to different screen sizes.
*   **Custom Scrollbars:** Styled scrollbars for a consistent look.

## Technologies Used

*   **HTML:** Structure of the web page.
*   **Tailwind CSS:** For styling the user interface. (CDN version used)
*   **JavaScript (Vanilla):** For all interactivity, including:
    *   Dynamically generating timeline elements from a data array (`ismetExperiences`).
    *   Calculating positions based on dates.
    *   Handling drag-and-drop functionality for cards.
    *   Drawing and updating SVG connector lines.

## File Structure

*   `cv.html`: The main HTML file containing the structure, styles (inline and Tailwind CSS), and JavaScript logic.

## How It Works

1.  **Data Source:** Experiences are defined in the `ismetExperiences` JavaScript array within the `cv.html` file. Each object in the array represents an event with properties like `id`, `type`, `label`, `startDate`, `endDate`, `color`, `description`, etc.
2.  **Timeline Generation:**
    *   A vertical axis representing years is drawn.
    *   Year markers are placed along this axis.
    *   For each experience in `ismetExperiences`:
        *   A duration bar is drawn on the main axis.
        *   A node (dot) is placed on the axis at the start date of the experience.
        *   An information card is created and positioned in a "lane" next to the timeline.
        *   An SVG line is drawn to connect the node on the axis to its corresponding card.
3.  **Interactivity:**
    *   **Drag and Drop:** Users can click and drag the information cards. The JavaScript updates the card's position and the end point of its SVG connector line in real-time.
    *   **Date Mapping:** Dates are converted into pixel positions on the timeline to ensure accurate placement.

## Setup

No special setup is required. Simply open the [`cv.html`](cv.html) file in a modern web browser.
