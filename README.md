A Github Pages template for academic websites. This was forked (then detached) by [Stuart Geiger](https://github.com/staeiou) from the [Minimal Mistakes Jekyll Theme](https://mmistakes.github.io/minimal-mistakes/), which is © 2016 Michael Rose and released under the MIT License. See LICENSE.md.

I think I've got things running smoothly and fixed some major bugs, but feel free to file issues or make pull requests if you want to improve the generic template / theme.

### Note: if you are using this repo and now get a notification about a security vulnerability, delete the Gemfile.lock file. 

# Instructions

1. Register a GitHub account if you don't have one and confirm your e-mail (required!)
1. Fork [this repository](https://github.com/academicpages/academicpages.github.io) by clicking the "fork" button in the top right. 
1. Go to the repository's settings (rightmost item in the tabs that start with "Code", should be below "Unwatch"). Rename the repository "[your GitHub username].github.io", which will also be your website's URL.
1. Set site-wide configuration and create content & metadata (see below -- also see [this set of diffs](http://archive.is/3TPas) showing what files were changed to set up [an example site](https://getorg-testacct.github.io) for a user with the username "getorg-testacct")
1. Upload any files (like PDFs, .zip files, etc.) to the files/ directory. They will appear at https://[your GitHub username].github.io/files/example.pdf.  
1. Check status by going to the repository settings, in the "GitHub pages" section
1. (Optional) Use the Jupyter notebooks or python scripts in the `markdown_generator` folder to generate markdown files for publications and talks from a TSV file.

See more info at https://academicpages.github.io/

## To run locally (not on GitHub Pages, to serve on your own computer)

1. Clone the repository and made updates as detailed above
1. Make sure you have ruby-dev, bundler, and nodejs installed: `sudo apt install ruby-dev ruby-bundler nodejs`
1. Run `bundle clean` to clean up the directory (no need to run `--force`)
1. Run `bundle install` to install ruby dependencies. If you get errors, delete Gemfile.lock and try again.
1. Run `bundle exec jekyll liveserve` to generate the HTML and serve it from `localhost:4000` the local server will automatically rebuild and refresh the pages on change.

# Changelog -- bugfixes and enhancements

There is one logistical issue with a ready-to-fork template theme like academic pages that makes it a little tricky to get bug fixes and updates to the core theme. If you fork this repository, customize it, then pull again, you'll probably get merge conflicts. If you want to save your various .yml configuration files and markdown files, you can delete the repository and fork it again. Or you can manually patch. 

To support this, all changes to the underlying code appear as a closed issue with the tag 'code change' -- get the list [here](https://github.com/academicpages/academicpages.github.io/issues?q=is%3Aclosed%20is%3Aissue%20label%3A%22code%20change%22%20). Each issue thread includes a comment linking to the single commit or a diff across multiple commits, so those with forked repositories can easily identify what they need to patch.


# Yahui Note

1. The google search history of this website is at https://search.google.com/search-console/performance/search-analytics?resource_id=https%3A%2F%2Fyahuisun.com%2F&breakdown=country

2. After changing the domin, you need to change "url                      :" in _config.yml

3. Change website title, go to "title                    : "Yahui Sun 孙亚辉"" in _config.yml

4. Change pages, go to "_data/navigation.yml"

5. Change first-page content, go to "_pages/about.md"

5. Change Publications page content, go to "academicpages/_pages/menu.md"  (permalink: /menu2/ is md file is used for navigation, not the name of md file)

6. Justify text in markdowns jekyll, "text-align: justify;" in "_sass/_base.scss"

7. Change font template size, text color etc., go to "_sass/_base.scss" and "_sass/_variables.scss"

8. code font size is in "_sass/_syntax.scss", as discussed in https://github.com/academicpages/academicpages.github.io/issues/59

8. Change main content font size: go to "body {
  font-size: $type-size-6;" in "_sass/_base.scss".
  
9. Change sidebar author content, go to "_config.yml" 

  
10. Change sidebar author content font size, go to "p, li {
    font-family: $sans-serif;
    font-size: $type-size-6;
    line-height: 1.5;
  }" in "_sass/_sidebar.scss".

11. Change Sitemap content, go to "_includes/footer.html"

12. Change general font size, change "body {
  font-size: $type-size-6;" in "_sass/_base.scss"
  
13. Make your Jekyll Github Pages appear on Google search result: https://victor2code.github.io/blog/2019/07/04/jekyll-github-pages-appear-on-Google.html
  
  
