---
    title:  "Five ways RO-Crate data packages are important for repositories"
    date: "2024-06-05"
    slug: open-repositories-2024-ro-crate
    categories: ["LDaCA"]
    tags: ["RO-Crate", "Open Repositories"]
    author: Peter Sefton
    toc:
      enable: true
      auto: true
---

<a href="2024-OR-RO-Crate.pdf">PDF version</a> | <a href="2024-OR-RO-Crate.pptx">Powerpoint Version</a>


<section typeof='http://purl.org/ontology/bibo/Slide'>
<img src='Slide00.png' alt='Five ways RO-Crate data packages are important for repositories :: Peter Sefton*, Stian Soiland-Reyes** ::  :: *University of Queensland, Australia; **The University of Manchester, UK ::  ::  :: ' title='Slide: 0' border='1'  width='85%%'/>



# Five ways RO-Crate data packages are important for repositories

Presented at: The 19th International Conference on Open Repositories, June 3-6th 2024, Göteborg, Sweden

Session: Presentations: Integrations for Research Data Management


Time: 05/June/2024: 11:00 - 12:30 · Location: Drottningporten 1

Peter Sefton*, Stian Soiland-Reyes**

*University of Queensland, Australia; **The University of Manchester, UK

Research Object Crate is a linked data metadata packaging standard which has been widely adopted in research contexts. In this presentation, we will briefly explain what RO-Crate is, how it is being adopted worldwide, then go on to list ways that RO-Crate is growing in importance in the repository world:

- Uploading of complex multi-file objects means RO-Crate is compatible with any general-purpose repository that can accept a ZIP file (with some coding, repository services can do more with RO-Crates).

- Download for well-described data objects complete with metadata from a repository rather than just a ZIP or file with no metadata.

- Using RO-Crate metadata reduces the amount of customisation that is required in repository software, as ALL the metadata is described using the same simple, self-documenting linked-data structures, so generic display templates.

- Sufficiently well-described RO-Crates can be used to make data FAIR compliant, aiding in Findability, Accessibility, Interoperability and Reusability thanks to standardised metadata and mature tooling.

- And if you’re looking for a sustainable repository solution, there are tools which can run a repository from a set of static files on a storage service, in line with the ideas put forward by Suleman in the closing keynote for OR2023.

<br>


</section>



<section typeof='http://purl.org/ontology/bibo/Slide'>
<img src='Slide01.png' alt='Uploading of complex multi-file objects … :: ' title='Slide: 1' border='1'  width='85%%'/>



## Uploading of complex multi-file objects


RO-Crate [1], [2] is a data packaging format and can be used to put multiple data files together with their metadata into a package such as a ZIP, tar or disk image file. This means that as long as your repository can handle a ZIP file it can take RO-Crates.

RO-Crates enable data to travel with metadata.

Beyond simply allowing the upload of opaque RO-Crates, there are opportunities for repository software to recognise metadata in an uploaded package and to pre-populate built-in metadata forms and/or datastores. This is not a pattern the authors have seen widely implemented in comprehensive institutionally focussed repositories, although at the time of writing it is being explored in Dataverse and InvenioRDM/Zenodo. We would encourage repository developers to explore this further, particularly those working with research data. RO-Crate support is increasing in research-domain repositories; e.g. RO-Crate upload with metadata extract is supported by WorkflowHub and ROHub).

<br>

</section>



<section typeof='http://purl.org/ontology/bibo/Slide'>
<img src='Slide02.png' alt='… is already supported even if the repo does not speak RO-Crate :: ' title='Slide: 2' border='1'  width='85%%'/>



One of the design features of an RO-Crate is that as it can be “just a ZIP file” it can be used with any old repository that can handle ZIP files. The JSON file can also be uploaded separately. As RO-Crate adoption increases, the repository may be able to start to use the RO-Crate metadata it already has. You can/will have heard from Dieuwertje Bloemen here at OR2024 that DataVerse has support for RO-Crate metadata preview and building import/export mechanisms.

<br>

</section>



<section typeof='http://purl.org/ontology/bibo/Slide'>
<img src='Slide03.png' alt='📂 ::  :: | :: |- ro-crate-metadata.json :: |-- Folder1/  :: |          |-- file1.this :: |          |-- file2.that :: |-- Folder2/ :: |		   -- file1.this :: |          |-- file2.that :: |-2021-04-08 07.58.17.jpg  :: { ::       &quot;@id&quot;: &quot;2021-04-08 07.58.17.jpg&quot;, ::       &quot;@type&quot;: &quot;File&quot;, ::       &quot;contentSize&quot;: 3271409, ::       &quot;dateModified&quot;: &quot;2021-04-08T07:58:17+10:00&quot;, ::       &quot;description&quot;: &quot;&quot;, ::       &quot;encodingFormat&quot;: [ ::         { ::           &quot;@id&quot;:  &quot;https://www.nationalarchives.gov.uk/PRONOM/x-fmt/391&quot; ::         }, ::         &quot;image/jpeg&quot; ::       ], ::       &quot;name&quot;: &quot;Cute puppy&quot; ::     }, ::  ::  RO-Crate Metadata Document :: ' title='Slide: 3' border='1'  width='85%%'/>



The RO-Crate specification described a method of packaging data in a folder, which can be zipped, with any kind of file.

This slide shows a folder of data, including a file with a typical obscure file name based on a timestamp (in this case created by a Dropbox upload from a digital camera). The RO-Crate Metadata file, in JSON Linked Data Format, can describe files. This one has a name (i.e. a title) for the file; “Cute puppy”.

<br>



</section>



<section typeof='http://purl.org/ontology/bibo/Slide'>
<img src='Slide04.png' alt='📂 ::  :: |-- Folder1/  :: |          |-- file1.this :: |          |-- file2.that :: |-- Folder2/ :: |		     |-- file1.this :: |          |-- file2.that :: |-2021-04-08 07.58.17.jpg  ::  :: ' title='Slide: 4' border='1'  width='85%%'/>



A human-readable description and preview (ro-crate-preview.html) can be in an HTML file that lives alongside the metadata. This slide shows an HTML view of the data that shows the image with its metadata, including the Schema.org `name` (equivalent to a Dublin Core `title`) for the file.

<br>

</section>



<section typeof='http://purl.org/ontology/bibo/Slide'>
<img src='Slide05.png' alt='' title='Slide: 5' border='1'  width='85%%'/>




Increasingly, research repository infrastructure is accepting RO-Crate input - this screenshot from WorkflowHub [documents the upload API[(https://about.workflowhub.eu/developer/ro-crate-api/) for submitting RO-Crate packaged descriptions of scientific workflows to the system. These can then be downloaded by others for reuse. Here, RO-Crate allows bypassing of the traditional “title, author, license, description” fields (rendered from the crate), as well as permitting user extensions on metadata to be kept in the repository.

<br>

</section>



<section typeof='http://purl.org/ontology/bibo/Slide'>
<img src='Slide06.png' alt='2.  RO-Crate is a packaging format suitable for downloads :: 2. :: ' title='Slide: 6' border='1'  width='85%%'/>



## RO-Crate is a packaging format suitable for downloads

One of the perennial problems with downloads is that once a user has the data, it often does not come with metadata as shown on the landing page, or if present it is in an ad hoc or specialised format. RO-Crate solves this by specifying an extensible way to put linked-data metadata with data assets and to provide an HTML page or small website with the data to explain it. Thus data travels *with* its metadata and can be made human-readable.

RO-Crate download is already available in many data repositories. Examples include:

*  [WorkflowHub](https://www.google.com/url?sa=t&source=web&rct=j&opi=89978449&url=https://workflowhub.eu/&ved=2ahUKEwi_wuuK9qmGAxWkAHkGHb9hDngQFnoECBgQAQ&usg=AOvVaw0Mgw-ytkMOTMLIPdH1AorW): A registry for describing, sharing and publishing scientific computational workflows.

*  [ROHub](https://www.rohub.org): A  repository of Earth Science datasets and computational methods.

*  [TLCMap](https://tlcmap.org/): The Time Layered Cultural map is a set of tools that work together for mapping Australian history and culture.

*  The [Language Data Commons of Australia data portal](https://data.ldaca.org.au): entirely built on RO-Crates, the underlying data consists of crates-on-disk and the API is based on RO-Crate metadata.

*  [Senckenberg Wildlive portal](https://wildlive.senckenberg.de/): exposes metadata about automatic photo captures of endangered animals using RO-Crate.

*  Dataverse: at the time of writing, RO-Crate downloads are in development.


We will encourage developers from other repository platforms to follow the Dataverse project’s lead and add RO-Crate support.

<br>

</section>



<section typeof='http://purl.org/ontology/bibo/Slide'>
<img src='Slide07.png' alt=' :: ' title='Slide: 7' border='1'  width='85%%'/>



This is a screenshot of the [Gazetteer of Historical Australian Places](https://uqz.zoom.us/j/85861337752) – not exactly a repository but an example of a place where people can download datasets.

<br>

</section>



<section typeof='http://purl.org/ontology/bibo/Slide'>
<img src='Slide08.png' alt='HTML Preview Describes the files :: ' title='Slide: 8' border='1'  width='85%%'/>


This kind of download could be added to any repository system where there is at least one file that has metadata; offer a download ZIP option that has machine-readable JSON metadata (linked data in JSON-LD) and a human-readable summary of the metadata – this one has descriptions of a few files in it.

<br>

</section>



<section typeof='http://purl.org/ontology/bibo/Slide'>
<img src='Slide09.png' alt='Enable programmatic downloads – include the metadata and its extensions :: signposting.org  :: ' title='Slide: 9' border='1'  width='85%%'/>



Every repository implementer should add FAIR Signposting – just a couple of HTTP headers – this means machines can go from an HTML landing page to the actual download without guesswork – or even better – to an RO-Crate! I’m sure you’ll hear this mentioned in one of the [talks](https://www.conftool.net/or2024/index.php?page=browseSessions&presentations=show&search=herbert) by Herbert van de Sompel and colleagues, such as the one on [FAIRiCat]. Again, DataVerse is ahead of the curve and has already implemented this.

[FAIRiCat]: https://www.conftool.net/or2024/index.php?page=browseSessions&form_session=475#paperID246 "FAIRiCat: Supporting Discovery of a Repository's Interoperability Affordances"

As we mentioned above, data should travel with the metadata – one example of this from the WorkflowHub is how other services like the LifeMonitor retrieves the RO-Crate and then looks for custom annotations in the metadata to pick up and connect to the testing infrastructure.  This was only possible because RO-Crate is extensible - you are not trapped with whatever 25 properties we’ve selected. The vessel is still RO-Crate, the repository didn't need to add anything to support the LifeMonitor.

<br>

</section>



<section typeof='http://purl.org/ontology/bibo/Slide'>
<img src='Slide10.png' alt='3. Less user interface customisation will be needed for different types of metadata :: ' title='Slide: 10' border='1'  width='85%%'/>



One of the key benefits of linked-data metadata over previous ‘legacy’ approaches, is that multiple vocabularies can be combined into a single metadata document in a way that is not possible with, say MARC, or MODS XML, and that all these vocabularies can use the same syntax and approach to describing data. This means that a simple generic RO-Crate viewer can be used to visualise any metadata whether it is basic “Who, What, Where” metadata (like Dublin Core) or domain-specific metadata like the RO-Crate metadata profile (https://w3id.org/ldac/profile) used by the Language Data Commons of Australia. This can be displayed alongside the core RO-Crate metadata without any expensive configuration or coding. If the recommendations are followed, the RO-Crate metadata terms are self-documenting, e.g. all the Language Data Commons terms which use a Schema.org Style approach, are defined here: https://w3id.org/ldac/terms.

<br>


</section>



<section typeof='http://purl.org/ontology/bibo/Slide'>
<img src='Slide11.png' alt=' ::  :: Here the mechanism is to use the ‘magic’ name METS.xml to store some extra metadata – with a fully linked-data system this kind of thing is not needed :: ' title='Slide: 11' border='1'  width='85%%'/>



This slide is a repeat of one we used last year – this screenshot is a bit of (undated) DSpace documentation found following a tip from Kim Sheppard – we have included it here to illustrate that storing additional metadata (in this case METS) for an object was done by convention – it had to be stored in a special file called METS.xml. Using a linked-data system means that we no longer have to do this kind of thing – there’s still one magic file name in RO-Crate but it’s only one for the metadata and one for the HTML preview – everything else is labelled and extensible.

<br>



</section>



<section typeof='http://purl.org/ontology/bibo/Slide'>
<img src='Slide12.png' alt=' ::  :: ' title='Slide: 12' border='1'  width='85%%'/>



This is an example of a data object in RO-Hub, which has a variety of files described in the object.


This site does not need to have multiple plugins for different kinds of data, as linked data has a generic structure. We saw another example of how the generic structure can be rendered in the opening example with a picture of Sefton's dog.

<br>

</section>



<section typeof='http://purl.org/ontology/bibo/Slide'>
<img src='Slide13.png' alt='No need to invent (completely) new file formats anymore! ::  ::  :: ' title='Slide: 13' border='1'  width='85%%'/>



So now we can tell all these research software developers, I know you like making new file formats, and I would love to support that in my repository, so could you perhaps use RO-Crate as the basis for making that format? Then we can pull out all the boring stuff, even for new file extensions, we just detect it’s a ZIP file and look for that magic file. If it says it’s an RO-Crate we’ll believe you.

<br>

</section>



<section typeof='http://purl.org/ontology/bibo/Slide'>
<img src='Slide14.png' alt='4. The availability of RO-Crate editing tools opens the way for repository software to focus on access and discoverability :: ' title='Slide: 14' border='1'  width='85%%'/>



The availability of RO-Crate editing tools opens the way for repository software to focus on access and discoverability.
We argue that the core functionality of a repository is keeping data safe and making it available with appropriate access controls (remember, not all data can be made Open Access - the A for accessibility in FAIR is about giving the right people (or other agents) access to the right data). RO-Crates require clear licensing statements to travel with data, and we will demonstrate how these have been integrated into access-control systems.


There is an opportunity, if RO-Crate is adopted as an interchange format, for the metadata editing functions (and authorisation) functions of a repository to be decoupled from it so the editor components for a particular metadata profile can be shared between repository instances, or handled in a more distributed architecture than in typical current repositories.

<br>

</section>



<section typeof='http://purl.org/ontology/bibo/Slide'>
<img src='Slide15.png' alt=' :: ' title='Slide: 15' border='1'  width='85%%'/>



The [Describo](https://describo.github.io/describo-users.html) website mentions this integration with the Dataverse repository where the Describo RO-Crate editor can be used to enter metadata. The pattern is potentially very powerful - separate the creation of metadata from the repository so that repositories can focus on data retention and multiple other applications can be built for use by researchers or other users – closer to or embedded in systems they are already using.

<br>

</section>



<section typeof='http://purl.org/ontology/bibo/Slide'>
<img src='Slide16.png' alt=' :: RO-Crate editing :: Data Portal :: ' title='Slide: 16' border='1'  width='85%%'/>



The Language Data Commons of Australia team has produced an alternative to Describo known as Crate-O – this is available as a web component ready to drop in to any web app or can function stand-alone  – we use it as part of the workflow in maintaining the [data portal for the Language Data Commons of Australia](https://data.ldaca.edu.au/collection?id=arcp%3A%2F%2Fname%2Cdoi10.26180%252F23961609&_crateId=arcp%3A%2F%2Fname%2Cdoi10.26180%252F23961609).

<br>



</section>



<section typeof='http://purl.org/ontology/bibo/Slide'>
<img src='Slide17.png' alt=' Portal shows that accessing this data requires authorisation. First step: Log in.' title='Slide: 17' border='1'  width='85%%'/>



This slide shows the beginning of an access-control process. The data was prepared in RO-Crate format using batch-processing scripts and has a license attached. The repository portal is shown here - with an indication that the user needs to log in to access the data.

<br>


</section>



<section typeof='http://purl.org/ontology/bibo/Slide'>
<img src='Slide18.png' alt=' logging in ' title='Slide: 18' border='1'  width='85%%'/>



The user logs in using CILogon (or another federated authentication service).

<br>

</section>



<section typeof='http://purl.org/ontology/bibo/Slide'>
<img src='Slide19.png' alt=' REMS ' title='Slide: 19' border='1'  width='85%%'/>



The user is then directed to an instance of REMS - the [Resource Entitlement Management System](https://github.com/CSCfi/rems/) (REMS) to request that a licence be granted to access the data. REMS is open-source software.

<br>

</section>



<section typeof='http://purl.org/ontology/bibo/Slide'>
<img src='Slide20.png' alt=' Applying for a license ' title='Slide: 20' border='1'  width='85%%'/>



After an approval process which may be automated, or may involve humans checking credentials, the user is directed back to the repository.

<br>

</section>



<section typeof='http://purl.org/ontology/bibo/Slide'>
<img src='Slide21.png' alt='5. With a repository to keep data safe and serve it using persistent Identifiers, RO-Crates help make data FAIR  :: ' title='Slide: 21' border='1'  width='85%%'/>



With a repository to keep data safe and serve it using persistent identifiers, RO-Crates help make data FAIR.

RO-Crate is increasingly being used to describe the provenance [3] of derived data in such a way that the workflows/computation that produced it can be re-run automatically to validate it, or as a basis for new research. This might be a button on a repository to run a bioinformatics workflow, or re-run a Jupyter notebook that produces a set of plots.

<br>


</section>



<section typeof='http://purl.org/ontology/bibo/Slide'>
<img src='Slide22.png' alt='' title='Slide: 22' border='1'  width='85%%'/>



RO-Crate helps to enable FAIR research practice; RO-Crates can describe inputs, outputs and code in any combination to record research processes, and can be used to provision services.

<br>

</section>



<section typeof='http://purl.org/ontology/bibo/Slide'>
<img src='Slide23.png' alt=' :: ' title='Slide: 23' border='1'  width='85%%'/>



This slide is a collage from a [presentation at eResearch Australasia](https://conference.eresearch.edu.au/wp-content/uploads/2023/11/1045-Alex-Ip.pdf), lead author Alex Ip put together showing some examples of code notebooks for text analytics and geophysics. Alex is working with the Language Data Commons of Australia team to make RO-Crate Profiles that can describe code, not just in terms of its authorship, language and inputs and outputs, but the (usually virtual) execution environment and hardware requirements needed to run it. This is a key step forward in the Interoperability and Reuse of data called for by the FAIR principles.

<br>



</section>



<section typeof='http://purl.org/ontology/bibo/Slide'>
<img src='Slide24.png' alt='6. (bonus point) There are tools which can run a repository from a set of static files on a storage service, in line with the ideas put forward by Prof Suleman at OR 2023 :: ' title='Slide: 24' border='1'  width='85%%'/>



There are tools which can run a repository from a set of static files on a storage service, in line with the ideas put forward by prof Suleman at OR 2023.
The team at the Language Data Commons of Australia, with partner institutions and colleagues, has been working to produce a set of tools for building Archival Repository software stacks that is based on a principled approach to keeping data safe, based on the principles presented in the Arkisto website[4] and more recently at <https://w3id.org/ldac/pilars> the core idea is that a collection of RO-Crates in a storage service can be the basis of a repository – either using a simple on-disk directory layout or something more complicated such as an Oxford Common File Layout (OCFL) specification.

<br>


</section>



<section typeof='http://purl.org/ontology/bibo/Slide'>
<img src='Slide25.png' alt='' title='Slide: 25' border='1'  width='85%%'/>



The [UTS Research Data Portal] is an example of a very minimal data repository system which uses a standard RO-Crate viewer to show RO-Crates that are sitting on file storage. This example is of an [engineering dataset](https://data.research.uts.edu.au/#view/0bacede4bd5a39993ec5088e6247cac8).

<br>

</section>



<section typeof='http://purl.org/ontology/bibo/Slide'>
<img src='Slide26.png' alt='The Language Data Commons of Australia Data Partnerships (LDaCA-DP), Language Data Commons of Australia Research Data Commons (LDaCA-RDC), and Australian Text Analytics Platform (ATAP) projects received investment (https://doi.org/10.47486/DP768, https://doi.org/10.47486/HIR001, &amp; https://doi.org/10.47486/PL074)  :: from the Australian Research Data Commons (ARDC).  ::  :: The ARDC is funded by the National Collaborative Research Infrastructure Strategy (NCRIS). :: ' title='Slide: 26' border='1'  width='85%%'/>


The Language Data Commons of Australia Data Partnerships (LDaCA-DP), Language Data Commons of Australia Research Data Commons (LDaCA-RDC), and Australian Text Analytics Platform (ATAP) projects received investment (https://doi.org/10.47486/DP768, https://doi.org/10.47486/HIR001, & https://doi.org/10.47486/PL074) from the Australian Research Data Commons (ARDC).

The ARDC is funded by the National Collaborative Research Infrastructure Strategy (NCRIS).





</section>
