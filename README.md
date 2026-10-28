# XML Link Dashboard

## Files
- index.html - Dashboard UI, CSS and JavaScript
- links.xml - Categories and links used by the dashboard

## Run locally

Because the browser may block XML loading when opening index.html directly, run a local web server.

### Python
```bash
python -m http.server 8000
```

Then open:
http://localhost:8000

## Features

- **Category & Link Management**: Add, edit, and delete categories and links directly in the browser UI.
- **Upload / Import XML**: Easily upload an existing `links.xml` file or paste XML markup directly.
  - **Replace Mode**: Overwrite all current categories and links.
  - **Merge Mode**: Combine new links into existing categories without removing current entries.
  - **Real-time Validation**: Validates XML structure and displays category and link counts before applying.
- **Export XML**: Download an updated `links.xml` or copy the generated XML to clipboard.
- **Local Storage Persistence**: Changes are automatically saved locally and persist across page refreshes.
- **Reset to Default**: Instantly reset dashboard back to the base `links.xml`.

## Add a new category

Add this inside <dashboard> in links.xml:

```xml
<category name="Cloud" color="tools">
    <link>
        <title>AWS</title>
        <description>Amazon Web Services</description>
        <url>https://aws.amazon.com/</url>
    </link>
</category>
```

Available sample colors:
- development
- tools
- documentation
- project
- other

You can add unlimited categories and links without changing index.html.
