#  noteapp (keskeneräinen)


# Vue Practice App with Firebase and Firestore

This is a simple Vue.js application created for the purpose of practicing Vue.js concepts. The app is also integrated with Firebase for real-time database functionality using Firestore.

## Project Overview

### Technology Stack:
- Vue.js
- Firebase
- Firestore
  
## Features

### Basic Vue App:

The project serves as a basic Vue.js application designed for practice and learning purposes.

### Firebase Integration:

The app is connected to Firebase for various features such as authentication(coming later).

### Firestore Database:

Firestore is used as the database to store and retrieve data seamlessly.


# Getting Started

## Prerequisites

Before running the project locally, ensure that you have the following installed:

- Node.js
- Vue CLI

This template should help get you started developing with Vue 3 in Vite.

# Installation

1. Clone the repository:
   
```sh
git clone https://github.com/tapiotorsti/noteapp.git
```

2. Navigate to the project directory:

```sh
cd noteapp
```
3. Install dependencies:

```sh
npm install
```

4. Set up Firebase Configuration:
- Create a Firebase project at Firebase Console.
- Obtain the Firebase configuration values (API Key, Auth Domain, Project ID, etc.).
- Create a .env file at the root of your project and set the Firebase configuration variables:
  
```sh
VUE_APP_FIREBASE_API_KEY=your_api_key
VUE_APP_FIREBASE_AUTH_DOMAIN=your_auth_domain
VUE_APP_FIREBASE_PROJECT_ID=your_project_id
VUE_APP_FIREBASE_STORAGE_BUCKET=your_storage_bucket
VUE_APP_FIREBASE_MESSAGING_SENDER_ID=your_messaging_sender_id
VUE_APP_FIREBASE_APP_ID=your_app_id
VUE_APP_FIREBASE_MEASUREMENT_ID=your_measurement_id
```

5. Run the app:

```sh
npm run dev
```

## Recommended IDE Setup

[VSCode](https://code.visualstudio.com/) + [Volar](https://marketplace.visualstudio.com/items?itemName=Vue.volar) (and disable Vetur) + [TypeScript Vue Plugin (Volar)](https://marketplace.visualstudio.com/items?itemName=Vue.vscode-typescript-vue-plugin).

## Customize configuration

See [Vite Configuration Reference](https://vitejs.dev/config/).

## Project Setup

```sh
npm install
```

### Compile and Hot-Reload for Development

```sh
npm run dev
```

### Compile and Minify for Production

```sh
npm run build
```

### Lint with [ESLint](https://eslint.org/)

```sh
npm run lint
```
