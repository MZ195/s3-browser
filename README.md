# React S3-Object-Storage Web App

This is a React web application that provides a simple interface for interacting with an S3-compatible object storage system (e.g., AWS S3, MinIO, DigitalOcean Spaces, etc.). The frontend allows users to interact with the object storage through a clean and intuitive interface.

## Features

- **List Objects**: Display a list of objects stored in the S3-compatible storage.
- **View Object Metadata**: View metadata information about specific objects.
- **Download Objects**: Download objects from the S3-compatible storage.
- **Upload Files**: Upload files to the S3-compatible storage.
- **Delete Objects**: Delete objects from the storage.

## Prerequisites

To run this application, you'll need:

- Node.js and npm (or yarn) installed on your local machine.
- A running instance of the [FastAPI S3-Compatible Object Storage API](https://github.com/MZ195/s3-compatible-api).
- Access to an S3-compatible object storage service (e.g., AWS S3, MinIO, DigitalOcean Spaces, etc.).

## Setup

### 1. Clone the Repository

Start by cloning the repository to your local machine:

### 2. Install Dependencies

Install the necessary dependencies by running:

```bash
npm install
```

or, if you're using yarn:

```bash
yarn install
```

### 3. Start the Application

To start the React development server, run:

```bash
npm start
```

or, if you're using yarn:

```bash
yarn start
```

This will start the React app and open it in your default browser, usually at `http://localhost:3000`.

## Components

The web app is structured into several key components:

### 1. **FileUploader**:

- This component allows users to upload files to the S3-compatible object storage. It uses a simple file input and sends the file to the backend API.

### 2. **ObjectList**:

- This component lists the objects stored in the S3-compatible storage. It fetches the object list from the backend and displays each item with a button to download, view metadata, or delete.

### 3. **ObjectMetadata**:

- This component allows users to view metadata information about an individual object. It fetches the object metadata (such as size, last modified date, etc.) from the backend.

### 4. **ObjectDownload**:

- This component allows users to download an object from the S3-compatible storage. It triggers the download by fetching the object from the backend.

### 5. **ObjectDelete**:

- This component provides a delete button to remove an object from the storage. It sends a request to the backend API to delete the object.

## API Integration

The React app interacts with the FastAPI S3-compatible object storage API. The following API endpoints are used:

- **GET /objects**: List all objects in the storage.
- **GET /object_info**: Fetch metadata for an object.
- **GET /object**: Download a specific object.
- **POST /object**: Upload a file to the storage.
- **DELETE /object**: Delete a specific object from the storage.

## Error Handling

The app will display user-friendly error messages if any API operation fails, such as if an object fails to upload, download, or delete. The error messages are provided by the FastAPI backend and displayed in the UI to the user.

## CORS

The React app interacts with the FastAPI backend, and CORS (Cross-Origin Resource Sharing) is configured to allow all origins by default. You can restrict or modify the allowed origins from the FastAPI backend if needed.

## Build for Production

To build the app for production, use the following command:

```bash
npm run build
```

This will create an optimized production build in the `build` folder. You can then deploy the contents of this folder to your preferred static hosting service (e.g., Netlify, Vercel, GitHub Pages, etc.).
