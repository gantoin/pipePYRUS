# pipePYRUS

## Overview
pipePYRUS is a document digitization and transcription tool designed to convert scanned book pages into editable, digital text. This tool streamlines the process of turning physical documents into accessible and modifiable digital formats.

## Workflow Diagram (Mermaid)
```mermaid
graph LR
    A["Upload PDF: Scan of Book"] --> B["Convert to PNG: Page by Page"]
    B --> C["Select Relevant Pages: Skip Blank Pages"]
    C --> D["Transcript Text: Format Text"]
    D --> E["Transcription Progress Screen: Handle Errors"]
    E --> F["View Extracted Text"]
```

## Endpoints

### Upload Endpoint
- `POST /upload`
  - Description: Receives and stores the PDF file.

### PDF to PNG Conversion Endpoint
- `POST /convert`
  - Description: Converts the PDF into individual PNG images for each page.

### Pages Selection Endpoint
- `GET /pages`
  - Description: Returns a list of PNG images for review.
- `POST /pages/select`
  - Description: Receives the identifiers of the selected pages for transcription.

### Transcription Initiation Endpoint
- `POST /transcribe`
  - Description: Initiates text extraction and formatting from selected images.

### Transcription Status Endpoint
- `GET /transcription/status`
  - Description: Returns the status of the transcription process.

### Extracted Text Retrieval Endpoint
- `GET /transcription/{id}`
  - Description: Returns the extracted and formatted text.

### Error Handling Endpoint
- `GET /transcription/errors`
  - Description: Returns any errors encountered during transcription.

## Getting Started
To get started with pipePYRUS, clone this repository and follow the setup instructions in the documentation.

## Contributing
Contributions to pipePYRUS are welcome! Please read our contributing guidelines for more information.

## License
pipePYRUS is released under the [MIT License](LICENSE).
```

Ce README fournit une vue d'ensemble du projet, un schéma de workflow facile à comprendre grâce à Mermaid, une description des endpoints, et des sections pour démarrer, contribuer, et la licence. Vous pouvez l'adapter en fonction des spécificités et des besoins supplémentaires de votre projet.
