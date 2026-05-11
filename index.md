# Hiii, 

My name is Aneta. I’m a graphic designer and content creator.

I like to combine aesthetics with meaning and emotion.
I want to show you who I am and what kind of work I do.

- [More about me →](about-me/) 

![photo1](/assets/images/IMG_0048.heic)

# Homework 📚

[View homework →](homework/)

# SERPENTE

<!DOCTYPE html>
<html lang="en">
<head>
<meta charset="UTF-8">
<meta name="viewport" content="width=device-width, initial-scale=1.0">
<title>Serpente — How a Hairpin Turn Became a Logo</title>
<link rel="preconnect" href="https://fonts.googleapis.com">
<link rel="preconnect" href="https://fonts.gstatic.com" crossorigin>
<link href="https://fonts.googleapis.com/css2?family=Bowlby+One&family=Space+Mono:ital,wght@0,400;0,700;1,400&family=Lora:ital,wght@0,400;0,500;1,400&display=swap" rel="stylesheet">
<style>
  :root {
    --olive: #7f8b5b;
    --olive-light: #a2ad7b;
    --olive-dark: #5d6841;
    --offwhite: #fcf9f1;
    --cream: #e4dfd7;
    --wine: #9a1d1e;
    --wine-soft: #af474c;
    --ink: #1a1a1a;
    --muted: #6b6b6b;
  }

  * { box-sizing: border-box; margin: 0; padding: 0; }

  html {
    scroll-snap-type: y mandatory;
    scroll-behavior: smooth;
    overflow-x: hidden;
  }

  body {
    font-family: 'Lora', Georgia, serif;
    background: var(--offwhite);
    color: var(--ink);
    line-height: 1.6;
    overflow-x: hidden;
  }

  /* ===== GRAIN OVERLAY ===== */
  body::before {
    content: '';
    position: fixed;
    inset: 0;
    background-image: url("data:image/svg+xml,%3Csvg xmlns='http://www.w3.org/2000/svg' width='200' height='200'%3E%3Cfilter id='n'%3E%3CfeTurbulence type='fractalNoise' baseFrequency='0.85' numOctaves='2' /%3E%3C/filter%3E%3Crect width='100%25' height='100%25' filter='url(%23n)' opacity='0.35'/%3E%3C/svg%3E");
    opacity: 0.18;
    pointer-events: none;
    z-index: 9999;
    mix-blend-mode: multiply;
  }

  /* ===== SLIDE BASE ===== */
  .slide {
    min-height: 100vh;
    width: 100%;
    scroll-snap-align: start;
    scroll-snap-stop: always;
    display: flex;
    flex-direction: column;
    justify-content: center;
    align-items: center;
    padding: 4rem 2rem;
    position: relative;
    overflow: hidden;
  }

  .slide-inner {
    max-width: 780px;
    width: 100%;
    z-index: 2;
  }

  .slide-num {
    position: absolute;
    top: 2rem;
    right: 2rem;
    font-family: 'Space Mono', monospace;
    font-size: 0.8rem;
    letter-spacing: 0.1em;
    opacity: 0.5;
    z-index: 3;
  }

  .slide-label {
    font-family: 'Space Mono', monospace;
    font-size: 0.75rem;
    letter-spacing: 0.25em;
    text-transform: uppercase;
    color: var(--muted);
    margin-bottom: 1.5rem;
    display: inline-block;
    padding-bottom: 0.5rem;
    border-bottom: 2px solid var(--olive);
  }

  /* ===== TYPOGRAPHY ===== */
  h1.hero-title {
    font-family: 'Bowlby One', sans-serif;
    font-size: clamp(4rem, 14vw, 11rem);
    line-height: 0.85;
    color: var(--olive);
    text-transform: uppercase;
    letter-spacing: -0.02em;
    margin: 0;
    transform: scaleY(1.6);
    transform-origin: bottom;
  }

  h2.section-title {
    font-family: 'Bowlby One', sans-serif;
    font-size: clamp(2.5rem, 6vw, 4.5rem);
    line-height: 0.95;
    color: var(--ink);
    text-transform: uppercase;
    letter-spacing: -0.015em;
    margin-bottom: 2rem;
    transform: scaleY(1.4);
    transform-origin: bottom left;
  }

  h2.section-title.olive { color: var(--olive); }
  h2.section-title.wine { color: var(--wine); }

  p {
    font-size: clamp(1.05rem, 1.5vw, 1.25rem);
    margin: 1rem 0;
    max-width: 65ch;
  }

  p.lead {
    font-size: clamp(1.2rem, 2vw, 1.5rem);
    line-height: 1.5;
  }

  blockquote {
    font-family: 'Lora', serif;
    font-style: italic;
    font-size: clamp(1.4rem, 2.5vw, 2rem);
    line-height: 1.35;
    color: var(--olive-dark);
    border-left: 4px solid var(--olive);
    padding: 0.5rem 0 0.5rem 1.5rem;
    margin: 2rem 0;
    max-width: 30ch;
  }

  strong { color: var(--olive); font-weight: 600; }
  em { font-style: italic; }

  /* ===== INTRO SLIDE ===== */
  .slide-intro {
    background: var(--offwhite);
    text-align: left;
    justify-content: space-between;
    padding: 4rem 3rem 4rem 3rem;
  }

  .intro-top {
    width: 100%;
    display: flex;
    justify-content: space-between;
    align-items: flex-start;
    font-family: 'Space Mono', monospace;
    font-size: 0.85rem;
    letter-spacing: 0.1em;
    color: var(--muted);
  }

  .intro-bottom {
    width: 100%;
    display: flex;
    justify-content: space-between;
    align-items: flex-end;
    font-family: 'Space Mono', monospace;
    font-size: 0.85rem;
    color: var(--muted);
  }

  .hero-wrap {
    width: 100%;
    margin: auto 0;
  }

  .hero-subtitle {
    font-family: 'Lora', serif;
    font-style: italic;
    font-size: clamp(1.2rem, 2.2vw, 1.7rem);
    color: var(--ink);
    margin-top: 2rem;
    max-width: 30ch;
  }

  .serpentine-deco {
    position: absolute;
    right: -5%;
    top: 50%;
    transform: translateY(-50%);
    width: 45%;
    height: 60%;
    opacity: 0.15;
    z-index: 1;
  }

  /* ===== ALT SLIDE COLORS ===== */
  .slide-olive {
    background: var(--olive);
    color: var(--offwhite);
  }
  .slide-olive h2,
  .slide-olive strong { color: var(--offwhite); }
  .slide-olive .slide-label {
    color: var(--cream);
    border-bottom-color: var(--cream);
  }
  .slide-olive blockquote {
    color: var(--offwhite);
    border-left-color: var(--cream);
  }

  .slide-wine {
    background: var(--wine);
    color: var(--offwhite);
  }
  .slide-wine h2,
  .slide-wine strong { color: var(--offwhite); }
  .slide-wine .slide-label {
    color: var(--cream);
    border-bottom-color: var(--cream);
  }

  .slide-cream {
    background: var(--cream);
  }

  /* ===== IMAGE CONTAINER ===== */
  .image-frame {
    width: 100%;
    aspect-ratio: 16 / 10;
    background: var(--cream);
    border: 1px solid var(--olive);
    margin: 2rem 0;
    display: flex;
    align-items: center;
    justify-content: center;
    position: relative;
    overflow: hidden;
  }

  .image-frame img {
    width: 100%;
    height: 100%;
    object-fit: cover;
    display: block;
  }

  /* Placeholder shown when image is missing/broken */
  .image-frame img:not([src]),
  .image-frame img[src=""] {
    display: none;
  }

  .image-frame .placeholder {
    position: absolute;
    inset: 0;
    display: flex;
    align-items: center;
    justify-content: center;
    background-image:
      repeating-linear-gradient(
        45deg,
        transparent,
        transparent 8px,
        rgba(127, 139, 91, 0.08) 8px,
        rgba(127, 139, 91, 0.08) 9px
      );
    pointer-events: none;
  }

  .image-frame img[src]:not([src=""]) + .placeholder {
    display: none;
  }

  .image-caption {
    font-family: 'Space Mono', monospace;
    font-size: 0.85rem;
    color: var(--olive-dark);
    text-align: center;
    padding: 1rem 2rem;
    background: rgba(252, 249, 241, 0.9);
    max-width: 80%;
  }

  /* ===== KEY MOMENT (the realization slide) ===== */
  .key-word {
    font-family: 'Bowlby One', sans-serif;
    font-size: clamp(5rem, 18vw, 14rem);
    color: var(--wine);
    text-transform: uppercase;
    line-height: 0.85;
    letter-spacing: -0.03em;
    transform: scaleY(1.6);
    transform-origin: center;
    text-align: center;
    margin: 2rem 0;
  }

  .slide-wine .key-word { color: var(--offwhite); }

  /* ===== TAKEAWAYS LIST ===== */
  .takeaway {
    margin: 2.5rem 0;
    padding-left: 2.5rem;
    position: relative;
  }

  .takeaway-num {
    position: absolute;
    left: 0;
    top: 0;
    font-family: 'Bowlby One', sans-serif;
    font-size: 2rem;
    color: var(--wine);
    line-height: 1;
  }

  .takeaway h3 {
    font-family: 'Bowlby One', sans-serif;
    font-size: 1.3rem;
    text-transform: uppercase;
    letter-spacing: 0.02em;
    margin-bottom: 0.5rem;
    color: var(--olive-dark);
  }

  /* ===== COLOR PALETTE GRID ===== */
  .palette {
    display: grid;
    grid-template-columns: repeat(3, 1fr);
    gap: 0.5rem;
    margin: 2rem 0;
  }
  .swatch {
    aspect-ratio: 4 / 3;
    display: flex;
    align-items: flex-end;
    padding: 1rem;
    font-family: 'Space Mono', monospace;
    font-size: 0.75rem;
    color: var(--offwhite);
  }
  .swatch.s1 { background: var(--olive); }
  .swatch.s2 { background: var(--offwhite); color: var(--olive-dark); border: 1px solid var(--olive); }
  .swatch.s3 { background: var(--wine); }
  .swatch.s4 { background: var(--olive-light); }
  .swatch.s5 { background: var(--cream); color: var(--olive-dark); border: 1px solid var(--olive); }
  .swatch.s6 { background: var(--wine-soft); }

  /* ===== FONT SAMPLES ===== */
  .font-sample {
    padding: 1.5rem;
    margin: 1rem 0;
    background: var(--offwhite);
    border-left: 4px solid var(--olive);
  }
  .font-sample.thunder {
    font-family: 'Bowlby One', sans-serif;
    font-size: 2.5rem;
    text-transform: uppercase;
    transform: scaleY(1.4);
    transform-origin: left;
    line-height: 0.9;
    color: var(--olive);
  }
  .font-sample.mono {
    font-family: 'Space Mono', monospace;
    font-size: 1rem;
    color: var(--ink);
  }
  .font-meta {
    font-family: 'Space Mono', monospace;
    font-size: 0.7rem;
    text-transform: uppercase;
    letter-spacing: 0.15em;
    color: var(--muted);
    margin-top: 0.5rem;
  }

  /* ===== ENDING ===== */
  .ciao {
    font-family: 'Bowlby One', sans-serif;
    font-size: clamp(6rem, 18vw, 14rem);
    color: var(--offwhite);
    text-transform: uppercase;
    line-height: 0.85;
    transform: scaleY(1.6);
    transform-origin: bottom;
    margin: 2rem 0;
  }

  .signature {
    font-family: 'Lora', serif;
    font-style: italic;
    font-size: 1.2rem;
    color: var(--cream);
    margin-top: 3rem;
  }

  /* ===== NAVIGATION DOTS ===== */
  .nav-dots {
    position: fixed;
    right: 1.5rem;
    top: 50%;
    transform: translateY(-50%);
    display: flex;
    flex-direction: column;
    gap: 0.6rem;
    z-index: 100;
  }
  .nav-dot {
