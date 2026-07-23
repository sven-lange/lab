+++
title = "Contact"
date = '2026-04-16T18:10:00-04:00'
draft = false
showDate = false
showAuthor = false
showReadingTime = false
showTableOfContents = false
+++

We welcome inquiries from prospective students, post-docs and collaborators.

<div class="mt-8 space-y-5">

<div class="contact-card rounded-2xl bg-white/80 p-6 shadow-sm backdrop-blur-sm dark:bg-neutral-900/45" data-scroll-reveal="fade-left">
  <h3 class="text-2xl font-bold text-neutral-900 dark:text-neutral-100">Sven M. Lange, Ph.D.</h3>
  <p class="mt-1 text-base italic text-neutral-700 dark:text-neutral-300">Assistant Professor</p>

  <div class="mt-5 flex flex-wrap items-center gap-4 text-neutral-600 dark:text-neutral-400">
    <a
      href="mailto:sml4006@med.cornell.edu"
      class="contact-link inline-flex items-center gap-2 transition hover:text-primary-700 dark:hover:text-primary-400">
      <span class="icon h-5 w-5">{{< icon "email" >}}</span>
      <span>sml4006@med.cornell.edu</span>
    </a>
    <a
      href="https://bsky.app/profile/sven-m-lange.bsky.social"
      target="_blank"
      rel="me noopener noreferrer"
      class="contact-link inline-flex items-center gap-2 transition hover:text-primary-700 dark:hover:text-primary-400">
      <span class="icon h-5 w-5">{{< icon "bluesky" >}}</span>
      <span>Bluesky</span>
    </a>
  </div>

  <div class="mt-6">
    <a href="https://biochem.weill.cornell.edu/" target="_blank" rel="noopener noreferrer">
      <img src="/img/WCM_BnB_logo.png"
           alt="Weill Cornell Biochemistry & Biophysics Logo"
           class="w-48 opacity-80 transition hover:opacity-100">
    </a>
  </div>
</div>

<div class="contact-card rounded-2xl bg-white/80 p-6 shadow-sm backdrop-blur-sm dark:bg-neutral-900/45" data-scroll-reveal="fade-left">
  <div class="flex flex-col gap-6 md:flex-row">
    <!-- NYC street video -->
    <div class="md:w-1/2">
      <div class="overflow-hidden rounded-xl">
        {{ $streetVideo := resources.Get "img/animations/332900_medium_pixabay_NYC_street.mp4" }}
        {{ if $streetVideo }}
          <video
            class="h-auto w-full object-cover"
            autoplay
            muted
            loop
            playsinline
            aria-hidden="true">
            <source src="{{ $streetVideo.RelPermalink }}" type="video/mp4">
          </video>
        {{ end }}
      </div>
    </div>

    <!-- Address and map -->
    <div class="flex flex-col justify-between md:w-1/2">
      <div>
        <h3 class="text-lg font-bold text-neutral-900 dark:text-neutral-100">Location</h3>
        <p class="mt-2 text-neutral-700 dark:text-neutral-300">
          Department of Biochemistry & Biophysics<br>
          Weill Cornell Medicine<br>
          1300 York Avenue<br>
          New York, NY 10065
        </p>
      </div>
      <div class="mt-4 overflow-hidden rounded-xl">
        <iframe
          title="Lange Lab location on OpenStreetMap"
          class="h-48 w-full border-0 sm:h-56"
          loading="lazy"
          referrerpolicy="no-referrer-when-downgrade"
          src="https://www.openstreetmap.org/export/embed.html?bbox=-73.9635%2C40.7635%2C-73.9575%2C40.7665&layer=mapnik&marker=40.7651%2C-73.9602">
        </iframe>
      </div>
    </div>
  </div>
</div>

</div>
