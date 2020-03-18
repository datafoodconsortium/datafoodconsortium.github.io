Official website and blog of the Data Food Consoriutm
=================================

[datafoodconsortium.org](http://datafoodconsortium.org/)

Powered by Jekyll

Deployed on Github Pages

Configured for CMS : [Forestry.io ](https://forestry.io/)


Website theme based on [Agency bootstrap theme ](https://startbootstrap.com/template-overviews/agency/)

=========

To access the forestry CMS, go to [datafoodconsortium.org/admin](http://datafoodconsortium.org/admin/) <br>

To add a post: Go to "posts" in the sidebar, click "add new post". In "Title", enter a short-version title (it's going to be in the url) and as "front matter template", choose "posts" (it should be selected by default). Click "Create" => In the "Title" field, replace the short version you entered before with the normal version of the title. Complete the other fields, got to the bottom of the page and start typing your article in the "body" section. When saving an article for the first time, it will be saved as "draft" by default, but you can simply switch off the toggle button "set as draft" and then hit "publish".

To add an image inside an article, simply add a blank line somewhere and a popup menu will appear. To add an "image credit" below an image, type anything like "image credit: John Doe" and format it to h3 => to format text (transform to title, add link etc...) simply select it and a popup menu will appear. Only use "h2" for titles inside an article. 


For more details, read the [jekyll documentation](http://jekyllrb.com/) and the [forestry.io documentation](http://forestry.io/docs/)


Ontology files need to be synchronized manually from https://github.com/datafoodconsortium/ontology. Basically you need to copy all the OWL files into the ontologies/ folder, then you create a Pull Request with these changes and merge it on the master branch of the main repository. Once merged, it is directly live on production.