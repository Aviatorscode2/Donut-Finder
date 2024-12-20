---
layout: page
---

# Installation

This guide provides the steps required to prepare your system for running tutorials for the **Donut Finder Service**, including setup, configuration, and verification of the environment.


> *Expected preparation time: Approximately 20 minutes.*

## Installation Types

This guide covers the following installation types:

| Type                   | Description                             | More information       |
| -----------------------|-----------------------------------------|------------------------|
|Local Development Setup | Setting up Donut Finder Service locally | See Installation Steps |

## Overview

This guide explains how to set up the Donut Finder Service, including:

- Cloning the project repository.
- Installing required dependencies.
- Testing the service on your local machine.

## Supported Versions

| Version | Build    | Release Date | Status    |
|---------|----------|--------------|-----------|
|v1.0     | Initial | 14/12/2024    | Stable    |

## System Requirements

Before installing, ensure your system meets the following requirements:

### Operating Systems
- Windows 10 or later
- macOS (latest or LTS version)
- Linux (latest or LTS version)

### Software Requirements

| Software       | Version               | Description      |
|----------------|-----------------------|------------------------|
|Node.js         | Current or LTS        | JavaScript runtime environment |
|json-server     | Current               | Simple REST API for JSON |
| Git            | Latest                | Version control system |
| Postman Desktop App | Latest           | API development tool |

## Installation Steps
Follow the steps below to set up the Donut Finder Service locally:

### Step 1: Clone the Repository
Clone the [Donut Finder](https://github.com/Aviatorscode2/Donut-Finder) repository to your local machine:
```bash
git clone https://github.com/Aviatorscode2/Donut-Finder.git
```
Navigate to the project directory:

```bash
cd Donut-Finder
```

### Step 2 - Open the Project
Open the project in your preferred code editor

### Step 3 - Start the Server
Navigate to the `api` folder and start the `json-server`:
```bash
cd api
json-server -w donuts-db.json
```
You should see the service running at `http://localhost:3000`.

## Verify Installation
To confirm the service is running correctly:

- Access `http://localhost:3000/donut-store` in a web browser or Postman.
- Verify that the API returns a list of donut stores.

## Post Installation

After completing the installation, you can:

- Explore the API endpoints using Postman.
- Start building your own features in the Donut Finder Service.

## Troubleshooting
### Problem: Server Not Starting

**Cause**: Missing or incorrectly installed dependencies.

**Solution**: Ensure `json-server` and Node.js are installed correctly. Reinstall if necessary:
```bash
npm install -g json-server
```

### Problem: No Response from API

**Cause**: The server is not running.

**Solution**: Restart the server in the `api` directory:
```bash
json-server -w donuts-db.json
```


## Next Steps

- Explore additional tutorials to extend the Donut Finder Service.

- Contribute to the project on [GitHub](https://github.com/Aviatorscode2/Donut-Finder.git).
