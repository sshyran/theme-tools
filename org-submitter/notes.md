Run through checklist and theme standards.
-- VIP scanner, maybe?

Test the theme with latest WP trunk install first, locally.
-- Probably doesn't need to be done, or would need to be done manually

Check package headers, fix if needed (see #1056-wpcom-themes).
-- Done via VIP scanner / should be done once, then forgotten

Update the readme.txt based on Trac changesets to give a brief history of changes.
-- Already done by wpcom download

Bump the version number in style.css.
-- DONE

Update Theme URI to the theme’s showcase page in `style.css`.
-- DONE

Ensure the theme has a POT file in the /languages directory; if not, generate a new GlotPress project for the theme with the following command on your sandbox, replacing [repo] and [theme-slug] accordingly, ie. pub/p2:
-- DONE
-- NEEDS TO RUN SCRIPT

php ~/public_html/bin/i18n/create-glotpress-project-for-theme.php /home/wpcom/public_html/wp-content/themes/[repo]/[theme-slug]


Commit any changes to our wpcom-themes repo.
-- TODO

Pull the theme from Showcase because it translates the wp.com lang files to .org format.

Add back tags in the style.css tags for the theme. Do not add WP.com specific tags such as all of Subjects and Styles, plus post-slider,  site-logo, and infinite-scroll under Features. You can see allowed tags on .org here.
-- DONE

Remove the updater.php file from /inc and call to it in functions.php.
-- DONE

Remove the -wpcom from the POT file.
-- DONE

Update the Underscores copyright year, if necessary.
-- DONE, in theory
// This seems to be stripped out of the themes generated by the downloader now... ?

Change the footer credit to the theme’s showcase page (WPTRT requires the credit to match either the Author URI or the Theme URI).
-- DONE

You need to zip all the theme files together. If you do this with Finder’s built in zip functionality you may end up with some extraneous files. So better do it from the Terminal: navigate to the theme directory and run zip -r THEMENAME.zip . -x "*/\.*"
-- TODO
