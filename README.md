# CSS Layouts and Responsive Design

## Objectives

Implement Flexbox and Grid for layout design.
<!DOCTYPE html>
<html lang="en">
<head>
  <meta charset="UTF-8">
  <meta name="viewport" content="width=device-width, initial-scale=1.0">
  <title>Flexbox + Grid Layout</title>
  <style>
    * {
      box-sizing: border-box;
      margin: 0;
      padding: 0;
    }

    body {
      font-family: Arial, sans-serif;
    }

    .container {
      display: grid;
      grid-template-areas:
        "header header"
        "sidebar main"
        "footer footer";
      grid-template-columns: 250px 1fr;
      grid-template-rows: auto 1fr auto;
      min-height: 100vh;
    }

    header {
      grid-area: header;
      background-color: #4CAF50;
      color: white;
      padding: 1rem;
      text-align: center;
    }

    aside {
      grid-area: sidebar;
      background-color: #f4f4f4;
      padding: 1rem;
    }

    main {
      grid-area: main;
      padding: 1rem;
      display: flex;
      flex-direction: row;
      gap: 1rem;
      flex-wrap: wrap;
    }

    .card {
      background-color: #e0e0e0;
      padding: 1rem;
      flex: 1 1 200px;
      border-radius: 8px;
      box-shadow: 0 2px 4px rgba(0,0,0,0.1);
    }

    footer {
      grid-area: footer;
      background-color: #333;
      color: white;
      text-align: center;
      padding: 1rem;
    }

    @media (max-width: 768px) {
      .container {
        grid-template-areas:
          "header"
          "main"
          "sidebar"
          "footer";
        grid-template-columns: 1fr;
      }
    }
  </style>
</head>
<body>

  <div class="container">
    <header>
      <h1>My Website</h1>
    </header>

    <aside>
      <h2>Sidebar</h2>
      <p>Navigation or widgets here.</p>
    </aside>

    <main>
      <div class="card">Card 1</div>
      <div class="card">Card 2</div>
      <div class="card">Card 3</div>
    </main>

    <footer>
      &copy; 2025 My Website
    </footer>
  </div>

</body>
</html>

Make the webpage responsive using media queries.<!DOCTYPE html>
<html lang="en">
<head>
  <meta charset="UTF-8" />
  <meta name="viewport" content="width=device-width, initial-scale=1.0"/>
  <title>Responsive Flexbox + Grid Layout</title>
  <style>
    * {
      box-sizing: border-box;
      margin: 0;
      padding: 0;
    }

    body {
      font-family: Arial, sans-serif;
      line-height: 1.6;
    }

    .container {
      display: grid;
      grid-template-areas:
        "header header"
        "sidebar main"
        "footer footer";
      grid-template-columns: 250px 1fr;
      grid-template-rows: auto 1fr auto;
      min-height: 100vh;
    }

    header {
      grid-area: header;
      background-color: #4CAF50;
      color: white;
      padding: 1rem;
      text-align: center;
    }

    aside {
      grid-area: sidebar;
      background-color: #f4f4f4;
      padding: 1rem;
    }

    main {
      grid-area: main;
      padding: 1rem;
      display: flex;
      flex-wrap: wrap;
      gap: 1rem;
    }

    .card {
      background-color: #e0e0e0;
      padding: 1rem;
      flex: 1 1 calc(33.333% - 1rem);
      border-radius: 8px;
      box-shadow: 0 2px 4px rgba(0,0,0,0.1);
    }

    footer {
      grid-area: footer;
      background-color: #333;
      color: white;
      text-align: center;
      padding: 1rem;
    }

    /* Tablet - under 992px */
    @media (max-width: 992px) {
      .card {
        flex: 1 1 calc(50% - 1rem);
      }

      .container {
        grid-template-columns: 200px 1fr;
      }
    }

    /* Mobile - under 768px */
    @media (max-width: 768px) {
      .container {
        grid-template-areas:
          "header"
          "main"
          "sidebar"
          "footer";
        grid-template-columns: 1fr;
      }

      main {
        flex-direction: column;
      }

      .card {
        flex: 1 1 100%;
      }
    }

    /* Extra small screens */
    @media (max-width: 480px) {
      header, footer, aside, main {
        padding: 0.75rem;
      }

      header h1 {
        font-size: 1.5rem;
      }

      .card {


Ensure proper alignment and spacing.
<!DOCTYPE html>
<html lang="en">
<head>
  <meta charset="UTF-8" />
  <meta name="viewport" content="width=device-width, initial-scale=1.0"/>
  <title>Responsive Layout with Flexbox & Grid</title>
  <style>
    * {
      box-sizing: border-box;
      margin: 0;
      padding: 0;
    }

    body {
      font-family: 'Segoe UI', sans-serif;
      line-height: 1.6;
      background-color: #f9f9f9;
      color: #333;
    }

    .container {
      display: grid;
      grid-template-areas:
        "header header"
        "sidebar main"
        "footer footer";
      grid-template-columns: 250px 1fr;
      grid-template-rows: auto 1fr auto;
      gap: 1rem;
      padding: 1rem;
      min-height: 100vh;
    }

    header {
      grid-area: header;
      background-color: #4CAF50;
      color: white;
      padding: 1.5rem;
      text-align: center;
      border-radius: 8px;
    }

    aside

## Instructions

- use Flexbox or CSS Grid.
- Add a navigation bar and structure the content.
- Use media queries to adjust layout for mobile, tablet, and desktop.

>[!NOTE]
>  - Include at least:
>  - navigation bar
>  - media queries

# Tasks

- Apply Flexbox or Grid for layout.
- Make the page responsive.
- Test across different screen sizes.

Happy Coding! 💻✨
