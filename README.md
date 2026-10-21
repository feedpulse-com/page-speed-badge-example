# Page Speed Badge — example

A live page-speed badge you can drop on any site with one script tag. Shows a real Google PageSpeed Insights score, refreshed weekly.

No signup. No API key. No build step. Works on any page that accepts HTML.

## Quick start

Paste this before `</body>`, swapping in the domain you want to measure:

```html
<script async src="https://feed-pulse.com/api/badge/speed.js?d=yourdomain.com"></script>
That's the whole install. The badge renders where you put the tag.

Options
Append any of these as query parameters:

Param	Values	Default
d	any domain or URL to measure	feed-pulse.com
sz	micro, sm, card, lg	card
theme	several light and dark themes	see the customizer
Example with options:

<script async src="https://feed-pulse.com/api/badge/speed.js?d=yourdomain.com&sz=micro"></script>
Where the number comes from
Google PageSpeed Insights, via its public API. Scores are Lighthouse lab data, so they reflect a synthetic test run rather than your real visitors — the same caveat applies to any Lighthouse-derived badge, including the one in PSI itself.

Results are cached and refresh weekly, so the badge will not re-measure on every page view.

Live customizer
Pick a theme and size, preview it, and copy the finished snippet: https://feed-pulse.com/free-page-speed-badge

Running this example
It is a single static HTML file. Open index.html in a browser, or serve the folder:

python3 -m http.server 8000
License
MIT


Scroll down, click **Commit changes**, keep the default message, confirm.

## Step 1.3 — Add index.html

Back on the repo home page: **Add file ▾ → Create new file**.

In the filename box type: `index.html`

Paste:

```html
<!doctype html>
<html lang="en">
<head>
  <meta charset="utf-8">
  <meta name="viewport" content="width=device-width, initial-scale=1">
  <title>Page Speed Badge — example</title>
  <style>
    body { font-family: ui-sans-serif, system-ui, sans-serif; max-width: 42rem; margin: 4rem auto; padding: 0 1.5rem; line-height: 1.6; }
    h1 { font-size: 1.5rem; margin-bottom: .25rem; }
    p { color: #555; }
    .badge-slot { margin: 2.5rem 0; }
  </style>
</head>
<body>
  <h1>Page Speed Badge</h1>
  <p>One script tag. Real PageSpeed Insights data, refreshed weekly.</p>

  <div class="badge-slot">
    <script async src="https://feed-pulse.com/api/badge/speed.js?d=feed-pulse.com"></script>
  </div>

  <p>Swap <code>d=</code> for your own domain. Themes and sizes:
     <a href="https://feed-pulse.com/free-page-speed-badge">customizer</a>.</p>
</body>
</html>
