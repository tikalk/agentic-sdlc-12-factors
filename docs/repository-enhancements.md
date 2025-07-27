# Repository Structure Enhancements

This document outlines the proposed enhancements to the repository structure to support internationalization (i18n), asset management, and improved development workflow.

## Internationalization (i18n) Structure

```
.
├── _i18n/
│   ├── en/
│   │   ├── content/
│   │   │   ├── strategic-mindset.md
│   │   │   ├── context-scaffolding.md
│   │   │   └── ... (other factors)
│   │   ├── manifesto.md
│   │   ├── playbook.md
│   │   └── manifesto-one-pager.md
│   ├── es/
│   │   └── ... (Spanish translations)
│   ├── fr/
│   │   └── ... (French translations)
│   └── ja/
│       └── ... (Japanese translations)
└── _config.yml (updated with i18n settings)
```

### I18n Implementation Details

1. Each language will have its own complete content structure
2. Default language (English) content will serve as the template
3. Language selector will be implemented in the theme header
4. URLs will follow the pattern: `/{lang}/path/to/content`
5. Default language (English) URLs can omit the language code

## Assets Directory Structure

```
.
├── assets/
│   ├── images/
│   │   ├── diagrams/
│   │   │   └── ... (architecture and flow diagrams)
│   │   ├── icons/
│   │   │   └── ... (site and factor icons)
│   │   └── logos/
│   │       └── ... (project logos and branding)
│   ├── css/
│   │   ├── custom.scss
│   │   └── ... (other style overrides)
│   ├── js/
│   │   └── ... (custom JavaScript if needed)
│   └── fonts/
│       └── ... (custom web fonts if needed)
```

### Asset Management Guidelines

1. All images should be optimized for web delivery
2. Use SVG format for icons and diagrams when possible
3. Maintain consistent naming conventions:
   - Use lowercase with hyphens
   - Include dimension suffixes for raster images (e.g., `logo-320w.png`)
   - Use descriptive, purpose-indicating names

## Version Control Considerations

1. Language-specific branches for translation work
2. Clear PR templates for content translation
3. Automated checks for missing translations
4. Regular sync of English content changes to other languages

## Implementation Priority

1. Set up assets directory structure
2. Implement i18n directory structure
3. Migrate existing content to English i18n directory
4. Update build configurations
5. Create documentation for translators