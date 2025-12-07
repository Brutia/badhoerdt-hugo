# Badhoerdt Hugo Site

This is a Hugo static site for the Badhoerdt badminton club.

## Prerequisites

- [asdf](https://asdf-vm.com/) package manager installed

## Installation

### Install Hugo using asdf

1. Install the Hugo plugin for asdf (if not already installed):
   ```bash
   asdf plugin add hugo
   ```

2. Install Hugo Extended (required version: 0.146.0 or higher):
   ```bash
   asdf install hugo latest
   ```

   Or install a specific version:
   ```bash
   asdf install hugo 0.146.0
   ```

3. Set Hugo as the local version for this project:
   ```bash
   asdf local hugo latest
   ```

   This will create/update the `.tool-versions` file with the Hugo version.

4. Verify the installation:
   ```bash
   hugo version
   ```

### Initialize Git Submodules

The project uses a theme as a git submodule. Initialize it with:

```bash
git submodule update --init --recursive
```

## Building the Project

### Development Server

To run the development server with live reload:

```bash
hugo server
```

The site will be available at `http://localhost:1313`

### Production Build

To build the site for production:

```bash
hugo
```

The generated static files will be in the `public/` directory.

### Build with Drafts

To include draft content in the build:

```bash
hugo -D
```

## Deployment

### Deploy via FileZilla

1. Build the site for production:
   ```bash
   hugo
   ```

2. Open FileZilla and connect to your FTP server.

3. Navigate to the `public/` directory in your local file system (left panel).

4. Navigate to your web server's root directory (typically `public_html`, `www`, or `htdocs`) in the remote server (right panel).

5. Upload all contents from the `public/` folder to the remote directory:
   - Select all files and folders in the `public/` directory
   - Drag and drop them to the remote directory, or right-click and select "Upload"

6. Wait for the upload to complete. Your site should now be live.
