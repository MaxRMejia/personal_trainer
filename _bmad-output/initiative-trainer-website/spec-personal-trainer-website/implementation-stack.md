# Implementation Stack

- Python generates a static site from Jinja2 templates and YAML or JSON content files.
- The build uses Pillow to resize images and convert them to WebP.
- Store trainer profile, service-area, contact, social profile URL, class, package, and gallery content in YAML or JSON; keep missing values as explicit placeholders until confirmed.
- Add the supplied Regal Power Fitness logo as a site asset and retain its red, black, and gold brand palette.
- Include the supplied agreement PDF in the static output and link a visible download button to it; visitors can save and print the file without server-side processing.
- YouTube and Instagram videos are embedded; video files are not self-hosted.
- Deploy the static output to Firebase Hosting free tier; expected traffic is under 200 visits per month.
- The first phase uses phone and email buttons. A contact form is deferred.