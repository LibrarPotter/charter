# Arceli 

## An archive of informal astronomy communications

Arceli was created in recognition that the Internet allows astronomers to publish useful material outside of traditional journals, yet there is no effective mechanism for these communications to be archived, indexed and cited (see [this Twitter conversation](https://storify.com/aaccomazzi/non-traditional-citations-in-astronomy) for Arceli's genesis).
Arceli acts as a facilitator for archiving communications on behalf of authors and providing a structure that NASA/SAO ADS can index.

This is a working document that specifies how Arceli will work.

## Overview

- Arceli is an archive of informal astronomy communications;
    * Arceli has an Editor and Board that is backed by astronomy libraries and the AAS or similar organizations,
    * Arceli is fundamentally a Zenodo curated community,
    * ADS agrees to index the resources of this Zenodo community,
    * [PressForward](http://pressforward.org/) is used to collect and discuss content
    * Online Publishers (such as a blog) apply for affiliation with Arceli. Each affiliated Publisher gains its own community within the umbrella Arceli community. This allows for self-moderation by Publishers while also giving oversight to Arceli. (Note: this community-in-a-community structure is an upcoming Zenodo feature).
    * Online publishers are given an account on PressForward in order to allow for self-moderation and community curation.
- The Publisher posts their content to the web as usual. The Publisher retains all rights to their work, but the content must be licensed to allow for archiving.
- Only if the Publisher deems the content to be relevant to scholarly astronomy discourse do they intentionally submit the content to the Zenodo community. This also implies that content can be retroactively submitted.
    * The submission consists of the work's source content. There is no prescribed format, but it should be easily and openly readable, e.g., plaintext/markdown and images or an ipython notebook. A PDF rendering could also be provided, secondarily.
    * The deposition is made into the Publisher's own Zenodo sub-community within Arceli's community via a submission form on Zenodo or through the REST API.
    * Arceli accepts the submission automatically because the Publisher is affiliated (trusted) and has its own community. This reduces Arceli's operational cost.
    * The Publisher gets a DOI for the content and it is up the Publisher to put this DOI into any online markup.
- ADS indexes Arceli's resources.
- If the Arceli Editor/Board finds a Publisher breaching its guidelines there is some mechanism for the Publisher to lose affiliate status and have articles removed from the Zenodo community and ADS.

## Governance

(stub)
whoever can talk the loudest/type the fastest gets their way.

## Moderation

[PressForward](https://github.com/PressForward/pressforward/wiki/User-Manual#using-the-all-content-page-how-to-read-nominate-and-add-comments-to-items) provides the platform for the editors to curate and discuss content.

TBD: who will actually moderate and make final go to publish.

### Accepted Subjects

(draft)
Anything relevant to the astronomy community that doesn't have a home elsewhere

### Not Accepted Subjects

(draft)
Scientific results that could otherwise be published on the arxiv. See discussion in [#6](https://github.com/archive-of-informal-astronomy-comm/charter/issues/6).

### Accepted Media

(draft)

- blog posts that contain text and images
- ipython notebooks which contain explanatory text
- videos - paper summaries, tutorials, etc.
- animations and graphics? - visuals which could be of use to wider community
- talk slides? - talk slides with relevance to the wider community.

### Not Accepted Media

(stub)

- pre-print style journal articles that would otherwise go on the arxiv

## Technical Aspects of Submitting to Arceli

PressForward site collects all the content via RSS feeds and allows it be moderated.

Content can be nominated manually with PressForward [Nominate This bookmarklet](https://github.com/PressForward/pressforward/wiki/User-Manual#installing-and-using-the-nominate-this-bookmarklet)

Workflow for Zenodo will borrow from [Making Your Code Citable](https://guides.github.com/activities/citable-code/).
A hook from PressForward WP will allow for communications to be deposited in Zenodo/Arceli communities after they are moderated/reviewed.

Arceli may provide some tools to ease the work of submitting content. LSST (@jonathansick) and others will probably make a Python tool for plaintext static blogs.

### Guidelines for Submission's content and format

It should be easily and openly readable, e.g., plaintext/markdown and images or an ipython notebook. 
If appropriate, a PDF rendering is encouraged.
[Something about URL and/or original blog.](https://github.com/archive-of-informal-astronomy-comm/charter/issues/5)

### REST Metadata Guidelines

Zenodo's [REST API specifies metadata](https://zenodo.org/dev#restapi-rep-meta) that can be included with a submission. This section provides some guidelines on how these fields should be used.

- `creators`. We mandate that the authors include an `orcid` field to encourage author disambiguation with [ORCID](http://orcid.org). The `affiliation` field is also mandated.
- `title` should match the original title of the work on the web.
- `publication_date` should be the date the work was originally published to the web.
- `description` will be mapped to the work's abstract on ADS. It can be drawn from the original content or be created for the deposition. It cannot be empty.
- `access_right` must be `'open'`. (Does it make sense to allow `closed` or `embargoed`?)
- `license` must be specified.
- `references`. Publishers must strive to properly cite material quoted or linked to through this field.
- `keywords`. Should we mandate a controlled keyword vocabulary?
- `upload_type`. We should allow any of these: `publication`, `poster`, `presentation`, `dataset`, `image`, `video`, `software`.
- `publication_type` if the material is a `publication`, such as a blog post, how do we describe that? `other`? `technicalnote`? `report`?
- `communities` must be the Publisher's own community within Arceli.
- `related_identifiers` should be automatically amended after submission to include the ADS bibcode.

## How ADS indexes Arceli

TBD

### Bibcode Format

(stub)

### BibTeX Format

(stub)

### Metrics that can be provided to and by ADS

(stub)
