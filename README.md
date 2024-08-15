# Tailwind-Setups
It will include all the integrated Tailwind project setups and demonstrate how to <mark>integrate tailwind to any project</mark>.

## Tailwind CSS Setup Guide
### Steps to Follow

1. **Navigate to Project Root**

    Move to your project’s root directory.

2. **Install Required Packages** 

    Install `tailwindcss`, `postcss`, and `autoprefixer` as dev dependencies:

    Use following command
    
        npm install -D tailwindcss postcss autoprefixer

3. **Generate Configuration Files**

    Generally we use following command

        npx tailwindcss init

    But there are some variation in above command using different flags that varies from project to project.

    1. Generate ESM config file using **--esm** flag.

        <code>npx tailwindcss init --esm</code>
    
    2. Generate TypeScript config file using **--ts** flag.

        <code>npx tailwindcss init --ts</code>

    3. Generate PostCSS configuration file alongside your tailwind.config.js file.

        <code>npx tailwindcss init -p</code>
    
        this will generate a **postcss.config.js** file

4. **Configure Content Sources**

    In this step, you need to specify which files Tailwind should consider. To do this, modify the **tailwind.config.js** file so Tailwind can identify the files that contain its classes. 

    Inside the **tailwind.config.js** file, you'll find a section called **content**. Add all the files that contain Tailwind classes to this section. These files can be of any type, such as **js, vue, ts, html, jsx, tsx, mdx**, etc. So simply add them like this:

        content: [

          "./**/*.{js,ts,jsx,tsx,mdx,html,vue,svelte}",
          "./**/*.{js,ts,jsx,tsx,mdx,html,vue,svelte}",
          "./**/*.{js,ts,jsx,tsx,mdx,html,vue,svelte}",
      
          // Or if files are in `src` directory:
          "./src/**/*.{js,ts,jsx,tsx,mdx,html,vue,svelte}",
        ],

        For more info, you can checkout this
        https://tailwindcss.com/docs/installation/framework-guides

5. **Create main.css**

    **main.css** file will going to contain all layers of tailwind.

        // You can give any name of your wish
        main.css

        // Add these lines to this file
        @tailwind base;
        @tailwind components;
        @tailwind utilities;

6. **Link main.css File**

    Link the **main.css** file in your project.

        For Example
      
        <!-- In Head section -->
        <link rel="stylesheet" href="~/src/main.css" />

        <!-- In configuration file -->
        css: ['~/src/main.css']

7. **Start Using Tailwind**

    You’re now ready to use Tailwind in your project.

