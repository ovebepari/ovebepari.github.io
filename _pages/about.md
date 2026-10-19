---
layout: default
title: About
permalink: /about/
---

<style>
  .about-wrapper {
    padding: 60px 24px 80px;
    max-width: 720px;
    margin: 0 auto;
  }

  .about-wrapper h1 {
    font-size: 1.6rem;
    font-weight: 300;
    letter-spacing: -0.02em;
    margin: 0 0 40px;
    color: var(--foreground);
  }

  .cards-grid {
    display: grid;
    grid-template-columns: 1fr 1fr;
    gap: 20px;
    margin-bottom: 40px;
  }

  .about-card {
    border: 0.5px solid var(--hairline);
    padding: 24px;
  }

  .about-card h3 {
    font-size: 0.7rem;
    text-transform: uppercase;
    letter-spacing: 0.1em;
    color: var(--muted);
    margin: 0 0 12px;
    padding-bottom: 8px;
    border-bottom: 0.5px solid var(--hairline);
  }

  .about-card p,
  .about-card blockquote {
    font-size: 0.85rem;
    line-height: 1.7;
    color: var(--foreground);
    margin: 0;
  }

  .about-card blockquote {
    font-style: italic;
    color: var(--muted);
    border: none;
    padding: 0;
  }

  .about-card.full-width {
    grid-column: 1 / -1;
  }

  .about-motto {
    margin-top: 40px;
    text-align: center;
  }

  .about-motto img {
    max-width: 100%;
    border: 0.5px solid var(--hairline);
  }

  .about-motto small {
    display: block;
    margin-top: 8px;
    font-size: 0.7rem;
    color: var(--muted);
    opacity: 0.6;
  }

  @media (max-width: 640px) {
    .cards-grid { grid-template-columns: 1fr; }
  }
</style>

<div class="about-wrapper">
  <h1>About</h1>

  <div class="cards-grid">
    <div class="about-card full-width">
      <h3>Bio</h3>
      <p>Curious about anything that makes me think harder. I learn one abstraction layer in computer science a year — slowly, deliberately. I spend too much time on the internet, notice other people's design choices before I notice their words, and believe sports and curiosity will save us all one day.</p>
    </div>

    <div class="about-card">
      <h3>Interests</h3>
      <p>System Programming · Computer Networking · Typography & Design · Photography · Field Recording · Cinema · Cooking · Cycling · Poetry · Geopolitics & Power Dynamics · Economics · Supply Chains</p>
    </div>

    <div class="about-card">
      <h3>Links</h3>
      <p><a href="https://github.com/ovebepari" target="_blank">GitHub</a> · <a href="https://linkedin.com/in/ovebepari" target="_blank">LinkedIn</a> · <a href="https://letterboxd.com/ovebepari/" target="_blank">Letterboxd</a> · <a href="mailto:codovi71@gmail.com">Email</a></p>
    </div>

    <div class="about-card full-width">
      <h3>William Martin</h3>
      <blockquote>
        Do not ask your children<br>
        to strive for extraordinary lives.<br>
        Such striving may seem admirable,<br>
        but it is the way of foolishness.<br>
        Help them instead to find the wonder<br>
        and the marvel of an ordinary life.<br>
        Show them the joy of tasting tomatoes, apples and pears.<br>
        Show them how to cry<br>
        when pets and people die.<br>
        Show them the infinite pleasure<br>
        in the touch of a hand.<br>
        And make the ordinary come alive for them.<br>
        The extraordinary will take care of itself.
      </blockquote>
    </div>

    <div class="about-card full-width">
      <h3>Watson Brothers</h3>
      <blockquote>
        চাইনা আমি সোনার চামচ আমারই মুখে<br>
        চাইনা আমি অসীম খ্যাতি আমার জগতে<br>
        আকাশের এই শূন্যতায় কত কি আছে<br>
        এক নিঃশ্বাসে মিশে যাই আকাশের সাথে<br>
        প্রায় ইচ্ছা করে আমার রাতের বেলাতে<br>
        ঘাসের মেঝেতে শুয়ে তারাদের দেখতে<br>
        সারা বিশ্ব হয়ে যায় আমার নিজের ঘর<br>
        খোলা আকাশের নিচে সবাই যাযাবর
      </blockquote>
    </div>
  </div>

</div>
