# Sumz

A OpenAI article summarizer application

### Things to Provide

- **public**: favicon.ico file
- **index.html**: Provide two font links, satoshi and inter
  ```html
  <!-- satoshi font family -->
  <link
     href="https://api.fontshare.com/v2/css?f[]=satoshi@1,900,700,500,300,400&display=swap"
     rel="stylesheet"
  />
  <!-- inter font family -->
  <link
     href="https://fonts.googleapis.com/css2?family=Inter:wght@100;200;300;400;500;600;700;800;900&display=swap"
     rel="stylesheet"
  />
  ```
- **tailwind.config**: Modify the config file to add these font families and the content
  ```javascript
  export default {
     content: ["./src/**/*.{html,js,jsx}"],
     theme: {
        extend: {
           fontFamily: {
              satoshi: ['Satoshi', 'sans-serif'],
              inter: ['Inter', 'sans-serif'],
           }
        },
     },
     plugins: [],
  }
  ```
- **App.css**: Contains the background styles along with some tailwind styles using [@apply directive](https://tailwindcss.com/docs/functions-and-directives#apply)
- **assets**: All the necessary icons/image files


### Notes
- Create a .env file and add it in the .gitignore. Get the Key from [RapidAPI Article Summarizer API](https://rapidapi.com/restyler/api/article-extractor-and-summarizer/)
  ```bash
  VITE_RAPID_API_ARTICLE_KEY=your_API_key
  ```
- Install redux toolkit and react redux
  ```bash
  npm install @reduxjs/toolkit react-redux
  ```
- Create the store & article file in the services folder and connect it with the application in main.js file
