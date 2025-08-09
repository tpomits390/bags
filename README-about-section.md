# About Section Component Integration Guide

## What's Created

I've created a promotional/about section component similar to the image you showed, with:

1. **Component File**: `src/views/components/home/about-section.twig`
2. **Styles**: Added to `src/assets/styles/04-components/home-blocks.scss`
3. **Example Usage**: `src/views/components/home/about-section-example.twig`

## How to Use

### Option 1: Add to Home Page

Create or edit a home component file to include this section:

```twig
{# Configure your section data #}
{% set about_data = {
  title: 'Mukhtmal',
  subtitle: 'stylish kids bags',
  about_title: 'About Velvet',
  content: 'Velvet is an innovative online store that aims to offer a range of modern and unique products that combine elegance and technology',
  image: asset('images/school-bag-supplies.jpg'),
  delivery_title: 'Delivery',
  delivery_jeddah: 'All over the Kingdom',
  delivery_time_jeddah: 'Jeddah: 1 to 3 business days.',
  delivery_time_other: 'Other regions: 1 to 6 days.',
  show_details_text: 'Show details',
  cta_text: 'Explore Our Collection',
  cta_link: '/products'
} %}

{# Include the component #}
{% include 'components.home.about-section' with {section: about_data} %}
```

### Option 2: Add to Existing Home Component

If you have existing home components, you can add this section to any of them by including:

```twig
{% include 'components.home.about-section' with {
  section: {
    title: 'Your Title',
    subtitle: 'Your Subtitle',
    content: 'Your content text...',
    image: asset('images/your-image.jpg')
  }
} %}
```

## Customization

### Image Requirements

- Add your main product image to `src/assets/images/` or `public/images/`
- Recommended size: 500x400px or similar aspect ratio
- Use PNG with transparency for best results

### Available Configuration Options

All options are optional with sensible defaults:

- `title`: Main heading (default: "Mukhtmal")
- `subtitle`: Subheading (default: "stylish kids bags")
- `about_title`: Section header (default: "About Velvet")
- `content`: Main description text
- `image`: Product image URL
- `delivery_title`: Delivery section title
- `delivery_jeddah`: Delivery coverage text
- `delivery_time_jeddah`: Jeddah delivery timeframe
- `delivery_time_other`: Other regions delivery timeframe
- `show_details_text`: Button text (default: "Show details")
- `cta_text`: Call-to-action button text (optional)
- `cta_link`: Call-to-action button link (optional)

### Styling Customization

The component uses Tailwind CSS classes and is fully responsive. You can customize:

- Colors by modifying the gradient classes (`from-yellow-400 to-yellow-500`)
- Spacing with padding/margin classes
- Typography with text size and weight classes
- Add your own CSS classes in the home-blocks.scss file

## Features

✅ **Fully Responsive** - Works on all device sizes
✅ **RTL Support** - Compatible with Arabic/RTL layouts  
✅ **Customizable** - Easy to modify content and styling
✅ **Performance Optimized** - Lazy loading images
✅ **Accessible** - Proper semantic markup
✅ **Modern Design** - Clean, professional appearance

## Next Steps

1. Add your product image to the images folder
2. Customize the content to match your brand
3. Include the component in your desired page
4. Test on different screen sizes
5. Adjust styling if needed
