<script>
    import { MetaTags } from 'svelte-meta-tags'
  </script>

<slot />
  
<MetaTags
    title="meh."
    description="An endless loop of meh."
    openGraph={{
    url: 'https://meh-two.vercel.app',
    title: 'meh.',
    description: "An endless loop of meh.",
    images: [
      {
        url: 'https://meh-two.vercel.app/og.jpg',
        width: 1200,
        height: 630,
        alt: "meh - An endless loop of meh."
      },
    ],
  }}
  twitter={{
    cardType: 'summary_large_image',
    title: 'meh.',
    description: "An endless loop of meh.",
    image: 'https://meh-two.vercel.app/og.jpg',
  }}
/>