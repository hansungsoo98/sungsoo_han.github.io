---
layout: page
permalink: /cv/
title: Curriculum Vitae
nav: true
nav_order: 5
description: Sungsoo Han's curriculum vitae.
---

<style>
  .cv-page {
    --cv-accent: #b400b9;
    --cv-border: rgba(0, 0, 0, 0.12);
    padding-top: 1.4rem;
  }

  .cv-hero {
    display: flex;
    align-items: center;
    justify-content: space-between;
    gap: 1.5rem;
    margin-bottom: 1.4rem;
  }

  .cv-title {
    margin: 0;
    font-size: clamp(2rem, 5vw, 3.2rem);
    font-weight: 700;
    letter-spacing: 0;
  }

  .cv-author {
    margin: 0.35rem 0 0;
    color: var(--global-text-color-light);
    font-size: 1.05rem;
  }

  .cv-pdf-button {
    width: 5.4rem;
    height: 5.4rem;
    border: 1px solid var(--cv-border);
    border-radius: 50%;
    display: inline-flex;
    flex-direction: column;
    align-items: center;
    justify-content: center;
    gap: 0.15rem;
    color: var(--global-text-color);
    background: var(--global-bg-color);
    text-decoration: none;
    box-shadow: 0 0.5rem 1.8rem rgba(0, 0, 0, 0.06);
    transition:
      transform 160ms ease,
      border-color 160ms ease,
      color 160ms ease;
    flex: 0 0 auto;
  }

  .cv-pdf-button:hover {
    transform: translateY(-2px);
    border-color: var(--cv-accent);
    color: var(--cv-accent);
    text-decoration: none;
  }

  .cv-pdf-button i {
    font-size: 2rem;
    line-height: 1;
  }

  .cv-pdf-button span {
    font-size: 0.78rem;
    font-weight: 700;
    letter-spacing: 0;
  }

  .cv-viewer-shell {
    background: #2f2f2f;
    border-radius: 0.55rem;
    padding: 0 2.6rem;
    min-height: 76vh;
    box-shadow: inset 0 0 0 1px rgba(255, 255, 255, 0.04);
  }

  .cv-viewer {
    width: 100%;
    height: 82vh;
    min-height: 620px;
    border: 0;
    display: block;
    background: #ffffff;
  }

  .cv-fallback {
    margin: 0;
    padding: 2rem;
    background: #ffffff;
    color: #222222;
  }

  @media (max-width: 768px) {
    .cv-page {
      padding-top: 0.4rem;
    }

    .cv-hero {
      align-items: flex-start;
    }

    .cv-title {
      font-size: 2rem;
    }

    .cv-pdf-button {
      width: 4.4rem;
      height: 4.4rem;
    }

    .cv-viewer-shell {
      padding: 0;
      border-radius: 0.35rem;
    }

    .cv-viewer {
      height: 78vh;
      min-height: 520px;
    }
  }
</style>

<div class="cv-page">
  <header class="cv-hero">
    <div>
      <h1 class="cv-title">Curriculum Vitae</h1>
      <p class="cv-author">Sungsoo Han</p>
    </div>
    <a class="cv-pdf-button" href="{{ '/assets/pdf/Sungsoo_Han_CV.pdf' | relative_url }}" target="_blank" rel="noopener" aria-label="Open CV PDF">
      <i class="fa-solid fa-file-pdf" aria-hidden="true"></i>
      <span>PDF</span>
    </a>
  </header>

  <section class="cv-viewer-shell" aria-label="Curriculum vitae preview">
    <object class="cv-viewer" data="{{ '/assets/pdf/Sungsoo_Han_CV.pdf' | relative_url }}" type="application/pdf">
      <p class="cv-fallback">
        <a href="{{ '/assets/pdf/Sungsoo_Han_CV.pdf' | relative_url }}">Open Sungsoo Han CV PDF</a>
      </p>
    </object>
  </section>
</div>
