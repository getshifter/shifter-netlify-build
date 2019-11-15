# Shifter Deploy to Netlify

Shifter to Netlify build script.

<a href="https://app.netlify.com/start/deploy?repository=https://github.com/getshifter/shifter-netlify-build"><img src="https://www.netlify.com/img/deploy/button.svg" alt="Deploy to Netlify"></a>

# How to

tl;dr: You have to set up both a Netlify and a Shifter site. They interact and conenct by using a webhook. These steps are an overview of both.

## On Netlify
1. Deploy this to Netlify
1. Navigate to deploy settings, add a build hook
1. Name the build hook, we called ours "Shifter Artifact Webhook", save it
1. Copy the new build hook URL, e.g. "https://api.netlify.com/build_hooks/abc123"

## On Shifter
1. Migrate or launch a new WordPress site on Shifter
1. Select a plan that support webhooks
1. Navigate to webhook settings, paste your Netlify build hook URL, save it
1. Generate a new artifact

## Explained
This process does 2 things. First, it sets up a Netlify site with the required build settings and redirects. Those settings are located within the `netlify.toml` file and `build.sh`.

This is the most basic version of a deploy pipeline between Shifter and Netlify.