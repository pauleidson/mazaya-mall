<div align="center">

  <img src="https://mall.mazayacapital.com/static/logo.svg" alt="Mazaya Mall Logo" width="200" style="--webkit-filter:drop-shadow(5 5 15 #ffffff);filter:drop-shadow(5 5 15 #ffffff);"/>

  # **Mazaya Mall - Promotional Landing Page**

  A high-performance, bilingual promotional landing page for Mazaya Mall, designed for lead generation and showcasing a premier real estate investment in Sadat City, Egypt.

  [![HTML5](https://img.shields.io/badge/HTML5-E34F26?style=for-the-badge&logo=html5&logoColor=white)](https://developer.mozilla.org/en-US/docs/Web/Guide/HTML/HTML5)
  [![CSS3](https://img.shields.io/badge/CSS3-1572B6?style=for-the-badge&logo=css3&logoColor=white)](https://www.w3.org/Style/CSS/Overview.en.html)
  [![JavaScript](https://img.shields.io/badge/JavaScript-F7DF1E?style=for-the-badge&logo=javascript&logoColor=black)](https://developer.mozilla.org/en-US/docs/Web/JavaScript)
  [![GitHub Pages](https://img.shields.io/badge/Hosted%20On-GitHub%20Pages-222222?style=for-the-badge&logo=github&logoColor=white)](https://pages.github.com/)

</div>

---

## 🚀 Live Demo

### **[https://mall.mazayacapital.com](https://mall.mazayacapital.com)**

---

## ✨ Key Features

*   **Bilingual Interface**: Seamless switching between Arabic (RTL) and English (LTR) with full content and layout adaptation.
*   **Performance First**: Optimized for speed with techniques like asynchronous font loading and image optimization.
*   **Fully Responsive**: Flawless experience across all device viewports, from mobile to ultra-wide desktops.
*   **CRM Integration**: A robust lead-generation form connected directly to the `EngazCRM` webhook API.
*   **Modern UI/UX**: Professional design with smooth animations, scroll-based interactions, and a clean, intuitive layout.
*   **SEO & Accessibility**: Built with best practices for search engine visibility and user accessibility (ARIA labels, semantic HTML).
*   **Custom 404 Page**: A branded "Page Not Found" experience to maintain user engagement.

---

## 🛠️ Technologies & Rationale

This project was built from the ground up using core web technologies to ensure maximum performance, maintainability, and a lightweight footprint. No heavy frameworks were used.

| Technology | Purpose & Rationale |
| :--- | :--- |
| **HTML5** | Used semantic HTML for better structure, SEO, and accessibility. |
| **CSS3** | Leveraged modern CSS features like **Flexbox**, **Grid**, **Custom Properties** (Variables), and **Keyframe Animations** to create a responsive and dynamic layout without JavaScript dependencies for styling. |
| **Vanilla JavaScript (ES6+)** | All interactivity is powered by dependency-free JavaScript. Using the native `fetch` API for asynchronous calls, **Intersection Observer** for scroll-based animations, and **DOM manipulation** for the mobile menu and language switcher ensures the site is fast and lean. |

---

## 📂 Project Structure

The repository is organized logically, separating the page content from its static assets for clarity and ease of maintenance.

```
/
├── 📄 index.html              # Main landing page (entry point)
├── 📄 404.html                 # Custom "Page Not Found" error page
│
└─── 📁 static/                 # Directory for all static assets
     ├── 📜 ArbFONTS-*.ttf
     ├── 📜 JUST Sans-*.otf
     ├── 🖼️ hero-background.webp
     ├── 🖼️ logo.svg
     ├── 🖼️ ... (favicons, etc.)
     └── 📄 site.webmanifest    # PWA configuration file
```

> **Note:** For deployment, the file structure has been simplified in the provided code. In a larger project, CSS and JavaScript would be in their own subdirectories (`/static/css/`, `/static/js/`).

---

## ⚙️ Getting Started

This project requires no build tools or compilation steps.

1.  **Clone the repository:**
    ```bash
    git clone https://github.com/Ali-Mahmoud-Abdalluh/mazaya-mall.git
    ```

2.  **Navigate to the project directory:**
    ```bash
    cd mazaya-mall
    ```

3.  **Run locally:**
    Open the `index.html` file directly in your web browser. For the best experience (to avoid potential CORS issues with `fetch`), it is recommended to use a lightweight local server like the [Live Server](https://marketplace.visualstudio.com/items?itemName=ritwickdey.LiveServer) extension for VS Code.

---

## 🔌 Contact Form & API Integration

The landing page features a critical lead-generation form that integrates with an external CRM.

*   **Endpoint URL:** `https://api.engazcrm.net/webhook/integration/mazayacapital/4/8/1`
*   **HTTP Method:** `POST`
*   **Request Payload:** The form's JavaScript handler constructs a JSON object and sends it via the `fetch` API.

    **Example JSON Payload:**
    ```json
    {
        "full_name": "John Doe",
        "mobile": "01012345678",
        "email": "john.doe@example.com",
        "last_comment": "Lead from website form."
    }
    ```

*   **Functionality:** The submission logic provides clear user feedback with different button states:
    *   **Default:** "Send Message"
    *   **On Submit:** "Sending..." (with a loading spinner)
    *   **On Success:** "Sent Successfully!" (form clears, button turns green)
    *   **On Error:** "Submission Failed" (button turns red)



