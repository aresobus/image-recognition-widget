# Image Recognition Widget: 

![MIT License](https://img.shields.io/badge/License-MIT-yellow.svg)
![npm version](https://badge.fury.io/js/%40krampstudio%2Frecog.svg)
![Svelte](https://img.shields.io/badge/svelte-%23f1413d.svg?style=for-the-badge&logo=svelte&logoColor=white)
![TailwindCSS](https://img.shields.io/badge/tailwindcss-%2338B2AC.svg?style=for-the-badge&logo=tailwind-css&logoColor=white)

It is a sophisticated image recognition widget that utilizes the [Google Cloud Vision API](https://cloud.google.com/vision) to identify objects in images. This widget can be seamlessly integrated into any web project either as a standalone JavaScript library or as a component within a Svelte framework.

## Installation

### Setting Up the Demo Application

1. Clone the repository:
    ```bash
    git clone https://github.com/aresobus/image-recognition-widget.git
    cd image-recognition-widget
    npm ci
    ```

2. Configure your API key:
    - Complete the [Google Cloud Vision API setup](https://cloud.google.com/vision/docs/setup).
    - Acquire an [API Key](https://cloud.google.com/docs/authentication/api-keys) and enter it in `demo/config.json`.

3. Launch the demo application:
    ```bash
    npm start
    ```

### Using a Library

To install Recog in your project:
```bash
npm install @aresobus/image-recognition-widget
```

#### Vanilla JavaScript Integration

```javascript
import RecogWidget from '@aresobus/image-recognition-widget';

new RecogWidget({
  target: document.querySelector('.some-container'),
  props: {
    apiUrl: 'https://vision.googleapis.com/v1/images:annotate?key=<YOUR_VISION_API_KEY>'
  }
});
```

#### Svelte Component Integration

```javascript
<script>
  import RecogWidget from '@aresobus/image-recognition-widget';
  const apiUrl = 'https://vision.googleapis.com/v1/images:annotate?key=<YOUR_VISION_API_KEY>'
</script>

<RecogWidget {apiUrl} />
```

#### Styling with TailwindCSS

Library is styled using [TailwindCSS](https://tailwindcss.com/), ensuring a modern and clean look.

## Development

- To run unit tests:
  ```bash
  npm test
  ```

- To start the development server:
  ```bash
  npm dev
  ```

- To lint the code:
  ```bash
  npm lint
  ```

