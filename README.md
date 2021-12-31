Hi.bro
- 👋 Hi, I’m shy-share
- 👀 I’m interested in coding.
- 🌱 I’m currently learning java.

# Blog posts
<!-- BLOG-POST-LIST:START -->
name: Latest blog post workflow
on:
  schedule: # Run workflow automatically
    - cron: '0 * * * *' # Runs every hour, on the hour
  workflow_dispatch: # Run workflow manually (without waiting for the cron to be called), through the Github Actions Workflow page directly

jobs:
  update-readme-with-blog:
    name: Update this repo's README with latest blog posts
    runs-on: ubuntu-latest
    steps:
      - name: Checkout
        uses: actions/checkout@v2
      - name: Pull in dev.to posts
        uses: gautamkrishnar/blog-post-workflow@master
        with:
          feed_list: "https://shyblog.world/"
<!-- BLOG-POST-LIST:END -->




