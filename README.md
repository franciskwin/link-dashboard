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
