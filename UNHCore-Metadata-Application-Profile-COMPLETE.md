# UNHCore Metadata Application Profile

- [UNHCore Metadata Application Profile](#unhcore-metadata-application-profile)
  - [Introduction](#introduction)
  - [Acknowledgments](#acknowledgments)
  - [Versioning](#versioning)
    - [Version History](#version-history)
  - [License](#license)
  - [General Guidelines](#general-guidelines)
    - [Relevant Namespaces](#relevant-namespaces)
    - [Describing Objects](#describing-objects)
      - [Statement on Potentially Harmful Language in Object Description](#statement-on-potentially-harmful-language-in-object-description)
        - [Resources for Anti-racist and Conscious Metadata](#resources-for-anti-racist-and-conscious-metadata)
  - [Standards and Best Practices](#standards-and-best-practices)
    - [General Best Practices](#general-best-practices)
      - [Content Standards for Metadata](#content-standards-for-metadata)
        - [List of Content Standards](#list-of-content-standards)
      - [Data Value Standards](#data-value-standards)
        - [List of Data Value Standards](#list-of-data-value-standards)
      - [Structural Standards for Metadata](#structural-standards-for-metadata)
        - [General Points](#general-points)
        - [List of Structural Standards](#list-of-structural-standards)
      - [Syntax Standards](#syntax-standards)
        - [List of Syntax Standards](#list-of-syntax-standards)
  - [Property Tables](#property-tables)
    - [Explanation of Table Components](#explanation-of-table-components)
    - [Required](#required)
    - [Required for Serials](#required-for-serials)
    - [Recommended](#recommended)
    - [Optional](#optional)

## Introduction

In planning the future of metadata for the UNH library in anticipation of a system migration, the UNHCore Property Set was changed from the DCMI Terms List (which had been used for the eventual support of a linked data environment) to the original Dublin Core Metadata Element Set. This allows for the temporary migration to Digital Commons, the system currently used for our Scholars' Repository.

The UNHCore requirements are designed to identify the properties necessary for a user in a shared metadata environment to gain a basic understanding of a metadata record and what it describes. They are not format-specific, but rather identify those properties commonly needed across all formats. The names of properties used here are not prescriptive, but have been generalized to indicate the broadest meaning of the property that is necessary to encompass a variety of formats.<sup id="a1">[1](#f1)</sup> These guidelines are not intended to be a replacement for format- or project-specific metadata best practices within the UNH Library. It is likely that specific formats will require more robust metadata than that outlined here. Individual projects and units that are creating metadata should contact the Metadata Librarian (Jay L. Colbert) to discuss needs, as additional customization in the system is possible.

The organic environment of metadata continues to evolve and the standards and best practices outlined here may evolve along with it. Additions, changes and deletions to this document will be recorded in the version control table for the UNHCore.

<b id="f1">1:</b> While hosted in Digital Commons, the Display Labels are assigned by the system, with available customization upon consultation. [↩](#a1)

## Acknowledgments

This iteration of UNHCore could not have happened without the generous help and inspiration from these external sources:

- [The Digital Public Library of America's Metadata Application Profile and related documentation](https://pro.dp.la/hubs/documentation)
- [The DLF AIG Metadata Application Profile Clearinghouse Project](https://dlfmetadataassessment.github.io/MetadataSpecsClearinghouse/)
- [The Mountain West Digital Library, especially their GitHub Wiki](https://github.com/mountainwestdl/mwdl-map)
- Michael Stewart, University of Delaware Libraries, for sharing a working draft of their DPLA Hub MAP
- [Sunshine State Digital Network](https://sunshinestatedigitalnetwork.wordpress.com/), especially their [Metadata Participation Guidelines](https://docs.google.com/document/d/1gNFYVThDAKyn54h_AyAk3-KwkcTk0skqtvKjNYSsO9U/edit?usp=sharing) and [Inclusive Metadata & Conscious Editing Resources List](https://docs.google.com/document/d/1APavAd1p1f9y1vBUudQIuIsYnq56ypzNYJYgDA9RNbU/edit?usp=sharing)

## Versioning

UNHCore is prepared, changed, and maintained by Jay L. Colbert, Metadata & Discovery Strategy Librarian, [jay dot colbert at unh dot edu](mailto:jay.colbert@unh.edu). The standards are influenced by the expertise of Eleta Exline, Sarah Stinson, and Nikki Hentz. Version numbers use [Semantic Versioning 2.0.0](https://semver.org/) format.

### Version History

| Version | Date       | Created/Changed By                                                                                                                                                                                 | Changes                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                              |
| ------- | ---------- | -------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------- | -------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------- |
| 1.0.0   | 2015-12-10 | Prepared by Sherry Vellucci<br />Reviewed and revised by the Metadata Working Group:<br />Sherry Vellucci, Chair<br />Christina Bellinger<br />Elise Daniel<br />Eleta Exline<br />Meredith Ricker | Original                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                             |
| 2.0.0   | 2020-10-16 | Prepared by Jay L. Colbert<br />Metadata & Discovery Strategy Librarian<br />[jay dot colbert at unh dot edu](mailto:jay.colbert@unh.edu)                                                          | Significant overhaul in order to accommodate the standards of Digital Commons and DPLA, as well as a possible future system migration. This overhaul required switching to the original Dublin Core Metadata Element Set from DCMI Terms. Property display names, field names, and Dublin Core mappings align with Digital Commons while leaving room for crosswalking. Some properties do not have Dublin Core mappings, and some do not yet have field names. These will be solidified after consulting with Digital Commons; however, we are allowed to suggest the fields and mappings.<br />This version is a draft of the proposed final version 2 properties. |
| 2.1.0   | 2021-04-15 | Revised by Jay L. Colbert                                                                                                                                                                          | Expanded property tables and edited guidelines to better represent controlled vocabularies and standards used                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                        |

## License

© The University of New Hampshire Libraries

<a rel="license" href="http://creativecommons.org/licenses/by/4.0/"><img alt="Creative Commons License" style="border-width:0" src="https://i.creativecommons.org/l/by/4.0/88x31.png" /></a><br />This work is licensed under a <a rel="license" href="http://creativecommons.org/licenses/by/4.0/">Creative Commons Attribution 4.0 International License</a>.

## General Guidelines

The UNHCore Metadata Property Set consists of 27 descriptive elements. However, it is a living set and is subject to change according to need. Properties are either required, recommended, or optional. UNHCore has 10 required (if available) properties, 4 recommended properties, and 10 optional properties. There are also 3 additional required (if available) properties for serials.

### Relevant Namespaces

Namespaces are prefixes to metadata properties that indicate the scheme from which it is being used. Namespaces prevent confusion about properties that may be used in more than one schema. The UNHCore MAP references properties using the following namespaces:

dc: <http://purl.org/dc/elements/1.1/>

dcterms: <http://purl.org/dc/terms/>

dcmitype: <http://purl.org/dc/dcmitype/>

### Describing Objects

Despite its various standards, metadata creation is not an exact science. Although some properties have little to no ambiguity—such as file format—others leave much room for interpretation and variety. _Sometimes, judgments will have to be made on a case-by-case basis, describing and classifying resources in particular;_ the subject headings one person assigns for a resource might be different than those assigned by another. The creation of metadata requires interpretation, and therefore is highly subjective and political.

No decision made in metadata creation is a neutral act.

Whenever possible, use the language and phrasing the resource provides. For resources without text, do not over-interpret visual cues or coding relating to identity. _When in doubt, consistency is more important than textbook accuracy._ For collections, create templates to include unique rules/exceptions. If you are unsure how to describe or title an object, please consult Jay L. Colbert and Sarah Stinson for historical precedent, industry standards, and emerging trends.

#### Statement on Potentially Harmful Language in Object Description

The nature of language is that it naturally changes and evolves over time. This includes language used for identities, communities, acts, affects, ethnicities, and other such realms. In the case of marginalized peoples and related subjects, the language used for them by those in power is often harmful, as it does not come from the marginalized themselves. Preferred language that was not harmful at the time might be harmful to current sensibilities. And within marginalized groups, terminology can be a site of debate and discourse.

This poses unique challenges for description and classification in library collections. Controlled vocabularies, such as the Library of Congress Subject Headings, typically follow literary warrant, meaning that they create terms when the need arises for them, and the wording used for the terms depends on the context of the need. Controlled vocabularies are also slow to change. However, their use is crucial. Controlled vocabularies allow researchers to navigate collections by subject and find related resources. Controlled vocabularies also (in theory) remove ambiguity: the Library of Congress Subject Heading "Segregation" means a specific thing, and every resource that uses it uses it with that context.

Therefore, UNHCore uses multiple controlled vocabularies when possible and/or creates local keywords. This practice allows for the type of categorization needed for research while also giving space to historical terminology and current preferred/alternative terminology. Because we import these collections into our Primo VE discovery environment, we privilege Library of Congress authorities to provide consistency (unless otherwise stated). When adding additional vocabularies, list the preferred term before any harmful language. Finally, make a note about the language in the Comments field. A list of alternative vocabularies is in the Best Practices and Guidelines portion of this Metadata Application Profile.

##### Resources for Anti-racist and Conscious Metadata

Archives for Black Lives in Philadelphia, Anti-Racist Description Working Group. (2019). _Archives for Black Lives Philadelphia Anti-Racist Description Resources_. <https://archivesforblacklives.files.wordpress.com/2019/10/ardr_final.pdf>

Bone, C. ORCID: 0000-0003-4868-124X, Lougheed, B., Callison, C., La France, J., & Reilly, T. (2015). _Changes to Library of Congress Subject Headings Related to Indigenous Peoples: For use in the AMA MAIN Database_ \[Working Paper]. Unpublished. <https://doi.org/10.5203/ss_ama.main_bon.chr.2015.1>

_Indigenous New Hampshire_. Indigenous New Hampshire. <https://indigenousnh.com/>

_Protocols for Native American Archival Materials_. <https://www2.nau.edu/libnap-p/protocols.html>

Society of American Archivists, Description Section. _Inclusive Description_. <https://www2.archivists.org/groups/description-section/inclusive-description>

Sunshine State Digital Network. (2020). _Inclusive Metadata & Conscious Editing Resources_. <http://bit.ly/SSDNInclusiveMetadata>

## Standards and Best Practices

The General Best Practices section provides an introduction to basic metadata concepts, and is organized by different types of metadata standards. The standards included are vetted standards and other standards may be included as needed, provided that they go through a formal Decision Process.

### General Best Practices

When standards are used for metadata they enable data sharing and interoperability among different systems. Standards, best practices, and documentation will play an even greater role for library metadata as open access, linked data and the Semantic Web become more integrated with library practices. Four types of standards used for metadata are discussed below.

- Content Standards
- Data Value Standards
- Structural Standards
- Syntax Standards

#### Content Standards for Metadata

**Content standards** explain what information should be recorded when describing a particular type of resource and how that information should be recorded. Paired with structural standards for metadata, content standards improve the ability to share metadata records and the discoverability of resources. When similar resources are described consistently across metadata records, users are better able to understand and analyze search results. Metadata that is formatted inconsistently (ex. names recorded both as "Last name, First name" and "First name / Last name;" terms abbreviated or spelled out) impacts indexing and sorting, and users bear the burden of having to decipher confusing or incomplete results.
The choice of which content standard should be decided based on the type of resources that will be described in the collection and the intended audience for the materials, and may be influenced by the structural standard being used.

##### List of Content Standards

- _Cataloging Cultural Objects (CCO),_ a data content standard published by ALA, was written mostly by Visual Resource Curators for the cultural heritage community. It serves a similar purpose as RDA, but with special treatment for cultural objects like works of art, architecture, and artifacts.
- _Describing Archives: A Content Standard (DACS)_ is a content standard designed for single- and multi-level descriptions of archives, personal papers, and manuscripts, and can be applied to all material types.
- _Resource Description and Access (RDA)_ is the current cataloging content standard. Selecting metadata properties according to RDA creates metadata for digital collections that are more readily interoperable with the library catalog bibliographic data.

#### Data Value Standards

**Data Value Standards** provide a normalized list of terms to be used for certain data elements. Using controlled terms ensures consistency between records and allows for collocation of resources related to the same topic or person. This is done through the use of thesauri, controlled vocabularies, and authority files. Data value standards are indicated for each UNHCore property where applicable.

##### List of Data Value Standards

- The AFS [American Folklore Society Ethnographic Thesaurus](https://id.loc.gov/vocabulary/ethnographicTerms.html) (version 2.3) is a vocabulary that can be used to improve access to information about folklore, ethnomusicology, ethnology, and related fields. The American Folklore Society developed the Thesaurus in cooperation with the American Folklife Center of the Library of Congress and supported by a generous grant from the Scholarly Communications Program of the Andrew W. Mellon Foundation.
- The [DCMI Type Vocabulary (DCMIType)](http://purl.org/dc/dcmitype/) provides a general, cross-domain list of approved terms that may be used as values for the Resource Type property to identify the genre of a resource.
- [DPLA Geographic and Temporal Guidelines for MAP 3.1](http://bit.ly/dpla-geo-styleguide-3_1): Recommendations for the formatting of geographic and temporal data in records that will be shared with DPLA.
- [DPLA Metadata Quality Guidelines](http://bit.ly/dpla-metadata-qual): Best practices for creating shareable metadata for the DPLA aggregation. Each property in the DPLA Metadata Application Profile is reviewed with tiered recommendations for minimal, improved, and best quality.
- [DPLA Standardized Rights Statements Implementation Guidelines](http://bit.ly/dpla-rights-guidelines): A description of DPLA's implementation of standardized rights statements and recommendations for the use of statements in records that will be shared with DPLA.
- [Getty Art and Architecture Thesauri (AAT)](http://www.getty.edu/research/tools/vocabularies/aat/) is a structured vocabulary for terms used to describe art, architecture, decorative arts, material culture, and archival materials.
- [Getty Thesaurus of Geographic Names (TGN)](http://www.getty.edu/research/tools/vocabularies/tgn/index.html) is a structured vocabulary for names and other information about places.
- [Getty Union List of Artist Names (ULAN)](http://www.getty.edu/research/tools/vocabularies/ulan/index.html) is a structured vocabulary for names and other information about artists.
- [Glossary of Disability Terminology](https://www.dpa.org.sg/wp-content/uploads/2015/10/DPA-Disability-Glossary-FINAL.pdf)
- [The Homosaurus](http://homosaurus.org)<sup id="a1">[1](#f1)</sup> is an international linked data vocabulary of LGBTQ terms that supports improved access to LGBTQ resources within cultural institutions. Designed to serve as a companion to broad subject term vocabularies, the Homosaurus is a robust and cutting-edge vocabulary of LGBTQ-specific terminology that enhances the discoverability of LGBTQ resources.
- [Internet Media Types (IMT—formerly known as MIME).](https://www.iana.org/assignments/media-types/media-types.xhtml) MIME types were originally created for emails sent using the SMTP protocol. Nowadays, this standard is used in a lot of other protocols, hence the new naming convention "Internet Media Type". See Appendix A for a list of Media Types.
- The [Library of Congress Genre/Form Terms](https://id.loc.gov/authorities/genreForms.html) for Library and Archival Materials (LCGFT) is a thesaurus that describes what a work is versus what it is about. For instance, the subject heading Horror films, with appropriate subdivisions, would be assigned to a book about horror films. A cataloger assigning headings to the movie The Texas Chainsaw Massacre would also use Horror films, but it would be a genre/form term since the movie is a horror film, not a movie about horror films. The thesaurus combines both genres and forms. Form is defined as a characteristic of works with a particular format and/or purpose. A "short" is a particular form, for example, as is "animation." Genre refers to categories of works that are characterized by similar plots, themes, settings, situations, and characters. Examples of genres are westerns and thrillers. In the term Horror films "horror" is the genre and "films" is the form.
- [Library of Congress Subject Headings (LCSH)](https://id.loc.gov/authorities/subjects.html) comprises a thesaurus of subject headings, maintained by the United States Library of Congress.
- [Library of Congress Name Authority File (LCNAF)](https://id.loc.gov/authorities/names.html) includes Corporate Names, Geographic Names, Conference Names and Personal Names.
- The [_OLAC video game genre vocabulary_](http://www.olacinc.org/olac-video-game-vocabulary) includes sixty-six genre terms, each with a scope note to help librarians choose the correct term when cataloging video games.
- [Queer LCSH](http://www.netanelganin.com/projects/QueerLCSH/QueerLCSH.html) is a project by Netanel Ganin which curates all Library of Congress Subject Headings relating to queer people.
- The [Thesaurus of Graphic Materials](https://id.loc.gov/vocabulary/graphicMaterials.html) is a tool for indexing visual materials by subject and by genre/format. The thesaurus includes more than 7,000 subject terms and 650 genre/format terms to index types of photographs, prints, design drawings, ephemera, and other pictures.
- [Virtual International Authority File (VIAF)](http://viaf.org) combines multiple name authority files into a single name authority service. The goal of the service is to lower the cost and increase the utility of library authority files by matching and linking widely-used authority files and making that information available on the Web.
- [The Women's Thesaurus](https://institute-genderequality.org/library-archive/thesaurus/) is a useful tool for searching by subject. It consists of terms about women, gender, gender equality and feminism. It also includes synonyms along with broader, more specific and related terms. The thesaurus is a good starting point for searches involving theses, research, articles, programs and policy memoranda.

<b id="f1">1:</b> Jay Colbert is a current member of the Homosaurus editorial board; you can reach out to him directly for questions relating to queer terminology and the use of the Homosaurus [↩](#a1)

#### Structural Standards for Metadata

**Metadata structure** includes the properties (aka fields or elements) where the data resides. Structural standards (i.e., metadata schemes) define the properties and the types of information that should be recorded in them. Since the UNHCore is based on the Dublin Core it is designed to be a structural standard with a lower level of granularity in order to accommodate most types of digital objects. When a higher level of granularity (i.e., more detail) is needed for a particular object or collection, properties may be added to the UNHCore and documented with an application profile. Sometimes the structural standards mandate what syntax standards should be used.

##### General Points

- Properties should be unambiguous.
- Some properties may be required.
- Some properties may be repeatable.
- Some properties may require a unique value, different from any other record in the system.
- Some properties may have defined relationships with other properties.

##### List of Structural Standards

- Dublin Core (DC) is the most widely used metadata standard to provide a basic level of description for interoperability at a low level of granularity. The UNHCore uses the original Dublin Core Metadata Element Set.

#### Syntax Standards

**Syntax standards** are used as the framework for the structural standards, supporting the exchange and sharing of data among different databases.

##### List of Syntax Standards

- Extensible Markup Language (XML) Extensible Markup Language is a simple, very flexible text format. Originally designed to meet the challenges of large-scale electronic publishing, XML is also playing an increasingly important role in the exchange of a wide variety of data on the Web.
- Resource Description Format (RDF) RDF is a standard model for data interchange on the Web. RDF has features that facilitate data merging even if the underlying schemas differ, and it specifically supports the evolution of schemas over time without requiring all the data consumers to be changed.

## Property Tables

_Note that the requirements of Digital Commons may be different than this MAP, especially where Dates and repeated fields are concerned. If Digital Commons requires something different than what is listed here, follow those requirements above this document. If possible in those situations, use this document to guide how that requirement is followed. Adjust any templates as necessary._

### Explanation of Table Components

| Label                   | Human-Readable Display Name of the Property                                                                                                                                                                                                          |
| ----------------------- | ---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------- |
| Definition              | Definition of the property                                                                                                                                                                                                                           |
| Dublin Core mapping     | The appropriate Dublin Core element and URI from <https://www.dublincore.org/specifications/dublin-core/dcmi-terms/>                                                                                                                                 |
| Digital Commons Field   | The input field name for the property in Digital Commons                                                                                                                                                                                             |
| Obligation              | Whether the property is required, recommended, or optional                                                                                                                                                                                           |
| Displayed               | Whether the property is displayed to end-users                                                                                                                                                                                                       |
| Repeatable              | Whether the property is repeatable, Yes/No                                                                                                                                                                                                           |
| Syntax/Formatting       | Guidance on how to format the values used in this element. If no syntax or formatting is recommended, this row will say "n/a."                                                                                                                       |
| Controlled Vocabularies | Recommended controlled vocabularies that can be used in this element. For full references and links to vocabularies, see [Standards and Best Practices](#standards-and-best-practices). If no vocabularies are recommended, this row will say "n/a." |
| How to Use              | Guidelines for what to put into an element and how to enter the data.                                                                                                                                                                                |
| Best Practices          | These guidelines represent the highest quality benchmarks recommended.                                                                                                                                                                               |
| Examples                | An example of the property in use                                                                                                                                                                                                                    |

### Required

- Creator\*
- Date
- Description
- File Format
- Identifier
- Language\*
- Rights
- Subject
- Title
- Type

| Label                   | Creator                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                               |
| ----------------------- | --------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------- |
| Definition              | Entity primarily responsible for making the described resource. May be a person(s), corporate body, or family.                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                        |
| Dublin Core mapping     | dc.creator ; <http://purl.org/dc/elements/1.1/creator>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                |
| Digital Commons Field   | author                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                |
| Obligation              | Required if available                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                 |
| Displayed               | Yes                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                   |
| Repeatable              | Yes                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                   |
| Syntax/Formatting       | If possible, place multiple names in separate instances of the element; otherwise, separate repeated terms consistently (e.g. with a semicolon).                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                      |
| Controlled Vocabularies | LCNAF, VIAF, ULAN, MARC Code List for Relators (for roles)                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                            |
| How to Use              | The name(s) of the creators of the item, such as authors, painters, or photographers.<br/>Agents like editors, translators, and illustrators go in the Contributors field.<br/>Editors of multi-chapter volumes are contributors, whereas the authors of the chapters are creators.<br/>Separate multiple creators with semicolons.                                                                                                                                                                                                                                                                                                                                                                                                                                   |
| Best Practices          | Use controlled vocabularies for names whenever possible. (Suggested controlled vocabularies can be found in [List of Content Standards](#list-of-content-standards). Also use local or regional controlled lists if available.)<br/>If names are not found in a controlled vocabulary, give the name in the following format: Last name, First name, Middle initial and period, year of birth and/or death if known, separated by a hyphen (e.g. Jones, Janet L., 1952-2019). (If dates are unknown, omit them).<br/>Avoid use of placeholder terms (e.g. "Unknown").<br/>Including terms to specify role is optional. If included, use a controlled vocabulary to indicate roles and maintain consistency. (Examples: author, co-author, photographer \[for images]) |
| Examples                | Haynes, Martin A. (Martin Alonzo), 1842-1919                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                          |

| Label                   | Date                                                                                                                                                                                                                                                                                                                                             |
| ----------------------- | ------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------ |
| Definition              | Date of creation of the original resource                                                                                                                                                                                                                                                                                                        |
| Dublin Core Mapping     | dc.date (dc.date.created) ; <http://purl.org/dc/elements/1.1/date>                                                                                                                                                                                                                                                                               |
| Digital Commons Field   | publication_date                                                                                                                                                                                                                                                                                                                                 |
| Obligation              | Required if available                                                                                                                                                                                                                                                                                                                            |
| Displayed               | Yes                                                                                                                                                                                                                                                                                                                                              |
| Repeatable              | No                                                                                                                                                                                                                                                                                                                                               |
| Syntax/Formatting       | Prefer use of YYYY-MM-DD format.<br/>For uncertain dates, can use "circa" or a question mark (?).<br/>For approximate dates, can use a tilde (~).<br/>As always, maintain consistent formatting as much as possible.                                                                                                                             |
| Controlled Vocabularies | EDTF, W3CDTF, ISO 8601                                                                                                                                                                                                                                                                                                                           |
| How to Use              | **Digital Commons only allows for YYYY, and the property is required.**<br/>Used for the date the original resource was created, not the date the item was digitized.<br/>If more than one date is used in the local system (e.g. digitization date, acquisition date), only the date of the original resource should be mapped to this element. |
| Best Practices          | Avoid using placeholder values (e.g. "Unknown". "n.d.").<br/>If possible, include a date range or approximate date.<br/>If no date is known, leave the element blank.<br/>For more information and examples, refer to DPLA's Geographic and Temporal Guidelines: <http://bit.ly/dpla-geo-styleguide>                                             |
| Examples                | 1969-06-29<br/>circa 1969<br/>1969?                                                                                                                                                                                                                                                                                                              |

| Label                   | Description                                                                                                                                                                                       |
| ----------------------- | ------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------- |
| Definition              | Description provides a free-text account of the resource that describes what the item is about. Includes but is not limited to a summary, an abstract, or a table of contents.                    |
| Dublin Core Mapping     | dc.description ; <http://purl.org/dc/elements/1.1/description>                                                                                                                                    |
| Digital Commons Field   | abstract                                                                                                                                                                                          |
| Obligation              | Required                                                                                                                                                                                          |
| Displayed               | Yes                                                                                                                                                                                               |
| Repeatable              | Yes                                                                                                                                                                                               |
| Syntax/Formatting       | _n/a_                                                                                                                                                                                             |
| Controlled Vocabularies | _n/a_                                                                                                                                                                                             |
| How to Use              | Describe the resource, such as what it is about and/or what it is, whichever is appropriate.<br/>Description should apply to the object being described, not to a collection to which it belongs. |
| Best Practices          | Remember that users will be seeing this description outside of its context, so avoid abbreviations and ambiguous references.                                                                      |
| Examples                | Man's vest of brown velveteen, machine-embroidered with pink flowers and green leaves.                                                                                                            |

| Label                   | File Format                                                                                   |
| ----------------------- | --------------------------------------------------------------------------------------------- |
| Definition              | The file format of the digital manifestation of the item                                      |
| Dublin Core mapping     | dc.format ; <http://purl.org/dc/elements/1.1/format>                                          |
| Digital Commons Field   | TBD                                                                                           |
| Obligation              | Required                                                                                      |
| Displayed               |                                                                                               |
| Repeatable              | No                                                                                            |
| Syntax/Formatting       | _n/a_                                                                                         |
| Controlled Vocabularies | [Internet Media Types (MIME)](https://www.iana.org/assignments/media-types/media-types.xhtml) |
| How to use              | Find the corresponding media type from the "Template" column in the MIME repositories         |
| Best Practices          | FYI: PDF is under the "application" registry                                                  |
| Examples                | application/pdf                                                                               |

| Label                   | Identifier                                                                      |
| ----------------------- | ------------------------------------------------------------------------------- |
| Definition              | The unique identifier for an item                                               |
| Dublin Core mapping     | dc.identifier ; <http://purl.org/dc/elements/1.1/identifier>                    |
| Digital Commons Field   | identifier                                                                      |
| Obligation              | Required                                                                        |
| Displayed               | No                                                                              |
| Repeatable              | No                                                                              |
| Syntax/Formatting       | _n/a_                                                                           |
| Controlled Vocabularies | _n/a_                                                                           |
| Standards               | The method of creating identifiers used by the Digital Collections              |
| How to Use              | Assign each item a unique identifier according to Digital Collections standards |
| Best Practices          | _n/a_                                                                           |
| Examples                | \|receiptsexpendit00dove\|~\|dover:0001                                         |

| Label                   | Language                                                              |
| ----------------------- | --------------------------------------------------------------------- |
| Definition              | The language of the resource                                          |
| Dublin Core mapping     | dc.language ; <http://purl.org/dc/elements/1.1/language>              |
| Digital Commons Field   | TBD                                                                   |
| Obligation              | Required if Available                                                 |
| Displayed               | Yes                                                                   |
| Repeatable              | No                                                                    |
| Syntax/Formatting       | _n/a_                                                                 |
| Controlled Vocabularies | [ISO 639-2](https://www.loc.gov/standards/iso639-2/php/code_list.php) |
| How to Use              | If the item has text, assign the item the language of the text        |
| Best Practices          | Not needed for most photographs unless they contain text              |
| Examples                | eng                                                                   |

| Label                   | Rights                                                                                                                                                                                                                             |
| ----------------------- | ---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------- |
| Definition              | Information about rights held in and over the described resource. Typically, rights information includes a statement about various property rights associated with the described resource, including intellectual property rights. |
| Dublin Core mapping     | dc.rights ; <http://purl.org/dc/elements/1.1/rights>                                                                                                                                                                               |
| Digital Commons Field   | rights                                                                                                                                                                                                                             |
| Obligation              | Required                                                                                                                                                                                                                           |
| Displayed               | Yes                                                                                                                                                                                                                                |
| Repeatable              | No                                                                                                                                                                                                                                 |
| Syntax/Formatting       | URI                                                                                                                                                                                                                                |
| Controlled Vocabularies | URI from <https://rightsstatements.org/>                                                                                                                                                                                           |
| How to Use              | Find the appropriate rights statement from <https://rightsstatements.org/> and use the URI given.                                                                                                                                  |
| Best Practices          | _n/a_                                                                                                                                                                                                                              |
| Examples                | <http://rightsstatements.org/vocab/InC/1.0/>                                                                                                                                                                                       |

| Label                   | Subject                                                                                                                                                                                                                                                                                                                                  |
| ----------------------- | ---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------- |
| Definition              | Topic of the item; what it is _about_                                                                                                                                                                                                                                                                                                    |
| Dublin Core mapping     | dc.subject ; <http://purl.org/dc/elements/1.1/subject>                                                                                                                                                                                                                                                                                   |
| Digital Commons Field   | TBD                                                                                                                                                                                                                                                                                                                                      |
| Obligation              | Required                                                                                                                                                                                                                                                                                                                                 |
| Displayed               | Yes                                                                                                                                                                                                                                                                                                                                      |
| Repeatable              | Yes                                                                                                                                                                                                                                                                                                                                      |
| Syntax/Formatting       | Separate subjects with commas. All nouns should be plural. Use sentence case except for proper nouns.                                                                                                                                                                                                                                    |
| Controlled Vocabularies | A controlled vocabulary such as AAT, LCSH, Homosaurus, or others as appropriate. For names and geographic locations, use name authority vocabularies. LCSH and other LoC vocabularies are preferred because of the Primo VE Discovery environment, but AAT and other Getty vocabularies in addition are recommended, especially for art. |
| How to Use              | Assign subjects based on what the resource is _about_, not what it _is_.                                                                                                                                                                                                                                                                 |
| Best Practices          | Split subdivided headings into individual headings with commas. If the subdivision is a genre or format, remove the subdivision and place in genre or medium as appropriate.                                                                                                                                                             |
| Examples                | Acworth (N.H. : Town) -- Appropriations and expenditures would turn into Acworth (N.H. : Town), Appropriates and expenditures<br/>Operas -- Scores would turn into Operas.                                                                                                                                                               |

| Label                   | Title                                                                                                                                         |
| ----------------------- | --------------------------------------------------------------------------------------------------------------------------------------------- |
| Definition              | Primary name given to the described resource.                                                                                                 |
| Dublin Core mapping     | dc.title ; <http://purl.org/dc/elements/1.1/title>                                                                                            |
| Digital Commons Field   | title                                                                                                                                         |
| Obligation              | Required                                                                                                                                      |
| Displayed               | Yes                                                                                                                                           |
| Repeatable              | No                                                                                                                                            |
| Syntax/Formatting       | _n/a_                                                                                                                                         |
| Controlled Vocabularies | _n/a_                                                                                                                                         |
| How to Use              | Transcribe the title exactly how it is presented on the resource.                                                                             |
| Best Practices          | Titles do not have to be unique.<br/>Try to avoid "Untitled", but do not interpret the the content to create a title; simple titles are okay. |
| Examples                | Muster Out Roll of the Second New Hampshire Regiment in the War of Rebellion                                                                  |

| Label                   | Type                                                                                                         |
| ----------------------- | ------------------------------------------------------------------------------------------------------------ |
| Definition              | What the _original_ resource is, _not_ the file format.                                                      |
| Dublin Core mapping     | dc.type ; <http://purl.org/dc/elements/1.1/type>                                                             |
| Digital Commons Field   | TBD                                                                                                          |
| Obligation              | Required                                                                                                     |
| Displayed               | Yes                                                                                                          |
| Repeatable              | No                                                                                                           |
| Syntax/Formatting       | _n/a_                                                                                                        |
| Controlled Vocabularies | [DCMI Type Vocabulary](https://www.dublincore.org/specifications/dublin-core/dcmi-terms/#section-7)          |
| How to Use              | Assign the resource a DCMI type, based on the original resource's carrier.                                   |
| Best Practices          | Scanned items are not automatically images. If the scanned image is a book, its type is Text, not StillImage |
| Examples                | Text                                                                                                         |

### Required for Serials

- Frequency
- Issue
- Volume

| Label                   | Frequency                                                                                                    |
| ----------------------- | ------------------------------------------------------------------------------------------------------------ |
| Definition              | The intervals at which the issues or parts of a serial or the updates to an integrating resource are issued. |
| Dublin Core mapping     | None suggested                                                                                               |
| Digital Commons Field   | TBD                                                                                                          |
| Obligation              | Required for Serials if Available                                                                            |
| Displayed               | Yes                                                                                                          |
| Repeatable              | No                                                                                                           |
| Syntax/Formatting       | _n/a_                                                                                                        |
| Controlled Vocabularies | None recommended                                                                                             |
| How to Use              | Describe how often the serial released updates                                                               |
| Best Practices          | _n/a_                                                                                                        |
| Examples                | Quarterly                                                                                                    |

| Label                   | Issue                                                                     |
| ----------------------- | ------------------------------------------------------------------------- |
| Definition              | The issue/number of the serial, or the monthly/seasonal identification    |
| Dublin Core mapping     | None suggested                                                            |
| Digital Commons Field   | issnum                                                                    |
| Obligation              | Required for Serials if Available                                         |
| Displayed               | Yes                                                                       |
| Repeatable              | No                                                                        |
| Syntax/Formatting       | Use numerals (5) rather than words (five)                                 |
| Controlled Vocabularies | None recommended                                                          |
| How to Use              | Transcribe the issue/number of the serial as it is stated on the resource |
| Best Practices          | _n/a_                                                                     |
| Examples                | 2                                                                         |

| Label                   | Volume                                                              |
| ----------------------- | ------------------------------------------------------------------- |
| Definition              | The volume number of the serial                                     |
| Dublin Core mapping     | None suggested                                                      |
| Digital Commons Field   | volume                                                              |
| Obligation              | Required for Serials if Available                                   |
| Displayed               | Yes                                                                 |
| Repeatable              | No                                                                  |
| Syntax/Formatting       | Use numerals (52) rather than words (fifty-two)                     |
| Controlled Vocabularies | None recommended                                                    |
| How to Use              | Transcribe the volume of the serial as it is stated on the resource |
| Best Practices          | None recommended                                                    |
| Examples                | 64                                                                  |

### Recommended

- Keywords
- Medium
- Place
- Publisher

| Label                   | Keywords                                                                                                   |
| ----------------------- | ---------------------------------------------------------------------------------------------------------- |
| Definition              | Local subject headings and keywords otherwise not represented by Subject.                                  |
| Dublin Core mapping     | dc.subject ; <http://purl.org/dc/elements/1.1/subject>                                                     |
| Digital Commons Field   | keywords                                                                                                   |
| Obligation              | Recommended                                                                                                |
| Displayed               | Yes                                                                                                        |
| Repeatable              | Yes                                                                                                        |
| Syntax/Formatting       | Nouns should be pluralized and verbs should be in -ing form.<br/>Use sentence case except for proper nouns |
| Controlled Vocabularies | _n/a_                                                                                                      |
| How to Use              | Enter multiple terms separated with commas.                                                                |
| Best Practices          | If possible, use existing vocabularies as templates/guides.                                                |
| Examples                | Boxes, Cats, Exploring                                                                                     |

| Label                   | Medium/Genre                                                                                                                                                                                                                            |
| ----------------------- | --------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------- |
| Definition              | The material, physical carrier, and/or genre of the resource.                                                                                                                                                                           |
| Dublin Core mapping     | dc.format.medium ; <http://purl.org/dc/elements/1.1/format>                                                                                                                                                                             |
| Digital Commons Field   | TBD                                                                                                                                                                                                                                     |
| Obligation              | Recommended                                                                                                                                                                                                                             |
| Displayed               | Yes                                                                                                                                                                                                                                     |
| Repeatable              | Yes                                                                                                                                                                                                                                     |
| Syntax/Formatting       | Nouns should be pluralized and verbs should be in -ing form. Use sentence case except for proper nouns. Separate multiple terms with commas.                                                                                            |
| Controlled Vocabularies | Controlled vocabularies such as AAT and LCGFT. Standards from the Library of Congress are preferred due to the Primo VE discovery environment.<br/>If medium/genre vocabularies are not sufficient, use subject vocabularies like LCSH. |
| How to Use              | Assign the resource a heading that represents the format of the physical resource itself, not the file format.<br/>Also use this property to describe the genre of a resource.                                                          |
| Best Practices          | When picking a vocabulary, use the one that is most appropriate for the collection. Town reports might use LCGFT/LCSH, whereas a photograph collection might use AAT.                                                                   |
| Examples                | battlefield maps, annual reports, bound sheet music                                                                                                                                                                                     |

| Label                   | Place                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                               |
| ----------------------- | ------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------- |
| Definition              | Spatial characteristics of described resource, such as a country, city, region, address or other geographical term. Captures aboutness.                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                             |
| Dublin Core mapping     | dc.coverage.spatial ; <http://purl.org/dc/elements/1.1/coverage>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                    |
| Digital Commons Field   | TBD                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                 |
| Obligation              | Recommended                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                         |
| Displayed               | Yes                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                 |
| Repeatable              | Yes                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                 |
| Syntax/Formatting       | Separate multiple terms with commas.                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                |
| Controlled Vocabularies | Controlled vocabularies, such as LCNAF, TGN, and GeoNames.<br/>Subject vocabularies may also be used.                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                               |
| How to Use              | Describe the place the resource is _about_ (or the place that is relevant), not where it was publishes/made.                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                        |
| Best Practices          | If the name of the place has changed over time, list the one used at the time/by the resource first.<br />If the place is on colonized or otherwise stolen land, list the indigenous territory name(s) first. Use the [Native Land](https://native-land.ca/) website to look up the territory names for specific locations; do not use any controlled vocabularies outside of the Native Land website and/or official land acknowledgments ([such as the Indigenous New Hampshire one](https://indigenousnh.com/land-acknowledgement/)). (It is encouraged to click the territory names given, as that will give more information, including a more complete name.) |
| Examples                | Pennacook, Wabanaki (Dawnland Confederacy), N'dakinna (Abenaki / Abénaquis), Dover (N.H.)                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                           |

| Label                   | Publisher                                                                                                                      |
| ----------------------- | ------------------------------------------------------------------------------------------------------------------------------ |
| Definition              | The agent responsible for publishing the resource.                                                                             |
| Dublin Core mapping     | dc.publisher ; <http://purl.org/dc/elements/1.1/publisher>                                                                     |
| Digital Commons Field   | publisher                                                                                                                      |
| Obligation              | Recommended                                                                                                                    |
| Displayed               | Yes                                                                                                                            |
| Repeatable              | No                                                                                                                             |
| Syntax/Formatting       | _n/a_                                                                                                                          |
| Controlled Vocabularies | Name authority files, such as LCNAF and VIAF.<br/>If a name authority file does not exist, use a subject heading such as LCSH. |
| How to Use              | Assign the resource an authorized version of the name of the publisher, taken from the resource.                               |
| Best Practices          | If there is no controlled term, create one by transcribing directly from the resource.                                         |
| Examples                | Boyd, William<br/>Penguin Random House                                                                                         |

### Optional

- Access Rights
- Alternative Title
- Comments
- Contributor
- Creative Commons License
- Extent
- Period of Relevance
- Rights Holder
- Scanning Information
- Source

| Label                   | Access Rights                                                      |
| ----------------------- | ------------------------------------------------------------------ |
| Definition              | The conditions under which the resource may be viewed or accessed. |
| Dublin Core mapping     | dc.rights.accessRights ; <http://purl.org/dc/elements/1.1/rights>  |
| Digital Commons Field   | TBD                                                                |
| Obligation              | Optional                                                           |
| Displayed               | Yes                                                                |
| Repeatable              | No                                                                 |
| Syntax/Formatting       | _n/a_                                                              |
| Controlled Vocabularies | _n/a_                                                              |
| How to Use              | Describe the access rights of the resource                         |
| Best Practices          | Use official statements and/or local statements when available     |
| Examples                | This collection is open.                                           |

| Label                   | Alternative Title                                                                                                                                                                                                                                                                                                                         |
| ----------------------- | ----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------- |
| Definition              | An alternative version of a title, such as a transliteration, translation, shorter, uniform, or commonly-known title(s).                                                                                                                                                                                                                  |
| Dublin Core mapping     | dc.title.alternative ; <http://purl.org/dc/elements/1.1/title>                                                                                                                                                                                                                                                                            |
| Digital Commons Field   | TBD                                                                                                                                                                                                                                                                                                                                       |
| Obligation              | Optional                                                                                                                                                                                                                                                                                                                                  |
| Displayed               | No                                                                                                                                                                                                                                                                                                                                        |
| Repeatable              | Yes                                                                                                                                                                                                                                                                                                                                       |
| Syntax/Formatting       | Use Title Case. Separate multiple titles with commas                                                                                                                                                                                                                                                                                      |
| Controlled Vocabularies | Check the "Use For" or "Variants" section of the official heading for suggestions                                                                                                                                                                                                                                                         |
| How to Use              | List alternative titles for the resource that would be helpful for a patron searching for the resource                                                                                                                                                                                                                                    |
| Best Practices          | Check the "Use For" or "Variants" section of the official heading for suggestions                                                                                                                                                                                                                                                         |
| Standards               | None suggested                                                                                                                                                                                                                                                                                                                            |
| Notes                   | Use for translations, transliterations, shorter, uniform title, or commonly-known titles. All titles should be in Title Case. Separate multiple alternative titles with semicolons.                                                                                                                                                       |
| Examples                | If the title of a score is _Le Nozze di Figaro,_ an alternative title could be _The Marriage of Figaro._ Alternatively, if the title of the score is _The Marriage of Figaro,_ you could put _Le Nozze di Figaro_ as an alternative title. For both, you could put the uniform title as an alternative title, which is _Nozze di Figaro._ |

| Label                   | Comments                                                                                                                                                                                                                                                                                                        |
| ----------------------- | --------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------- |
| Definition              | Any comments, notes, or additional information about the resource                                                                                                                                                                                                                                               |
| Dublin Core mapping     | dc.description ; <http://purl.org/dc/elements/1.1/description>                                                                                                                                                                                                                                                  |
| Digital Commons Field   | comments                                                                                                                                                                                                                                                                                                        |
| Obligation              | Optional                                                                                                                                                                                                                                                                                                        |
| Displayed               | Yes                                                                                                                                                                                                                                                                                                             |
| Repeatable              | No                                                                                                                                                                                                                                                                                                              |
| Syntax/Formatting       | _n/a_                                                                                                                                                                                                                                                                                                           |
| Controlled Vocabularies | _n/a_                                                                                                                                                                                                                                                                                                           |
| How to Use              | Give additional information that would be helpful for a patron, such as funding information.                                                                                                                                                                                                                    |
| Best Practices          | _n/a_                                                                                                                                                                                                                                                                                                           |
| Examples                | The Irma G. Bowen Historic Clothing Collection digital catalog was produced by the UNH Library Digital Collection Initiative, supported in part by a grant from the Mooseplate program and New Hampshire State Council on the Arts. Additional funding provided by the E. Ruth Buxton Stephenson Memorial Fund. |

| Label                   | Contributor                                                                                                                                                                                                                                                                                                                              |
| ----------------------- | ---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------- |
| Definition              | Agents who did not create the resource but contributed in other ways                                                                                                                                                                                                                                                                     |
| Dublin Core mapping     | dc.contributor ; <http://purl.org/dc/elements/1.1/contributor>                                                                                                                                                                                                                                                                           |
| Digital Commons Field   | TBD                                                                                                                                                                                                                                                                                                                                      |
| Obligation              | Optional                                                                                                                                                                                                                                                                                                                                 |
| Displayed               | Yes                                                                                                                                                                                                                                                                                                                                      |
| Repeatable              | Yes                                                                                                                                                                                                                                                                                                                                      |
| Syntax/Formatting       | Same as for Creator                                                                                                                                                                                                                                                                                                                      |
| Controlled Vocabularies | Name authority files such as LCNAF, VIAF, and GULAN. LCNAF is preferred due to the Primo VE environment.                                                                                                                                                                                                                                 |
| How to Use              | Use this property for agents like editors, illustrators, translators, and others who did not _create_ the resource.                                                                                                                                                                                                                      |
| Best Practices          | If there is no controlled version of the name whatsoever--or if a different person with the same name exists--construct a name as it appears on the resource as follows:<br/>FamilyName, GivenName (MiddleName or Initial if on the resource), DateOfBirth-DateOfDeath(if dead).<br/> Editors of multi-chapter volumes are contributors. |
| Examples                | Gabriel, Philip, 1953-                                                                                                                                                                                                                                                                                                                   |

| Label                   | Creative Commons License                                                                              |
| ----------------------- | ----------------------------------------------------------------------------------------------------- |
| Definition              | The Creative Common License that describes the copyright, license, and use conditions of the resource |
| Dublin Core mapping     | dc.rights.license ; <http://purl.org/dc/elements/1.1/rights>                                          |
| Digital Commons Field   | distribution_license                                                                                  |
| Obligation              | Optional                                                                                              |
| Displayed               | Yes                                                                                                   |
| Repeatable              | No                                                                                                    |
| Syntax/Formatting       | _n/a_                                                                                                 |
| Controlled Vocabularies | License Deed URI from [Creative Commons](https://creativecommons.org/licenses/)                       |
| How to Use              | Find the appropriate URI from <https://creativecommons.org/licenses/> and use the URI.                |
| Best Practices          | _n/a_                                                                                                 |
| Examples                | <https://creativecommons.org/licenses/by-nc/4.0/>                                                     |

| Label                   | Extent                                                                                                                                                               |
| ----------------------- | -------------------------------------------------------------------------------------------------------------------------------------------------------------------- |
| Definition              | The size and/or duration of the resource                                                                                                                             |
| Dublin Core mapping     | dc.format.extent ; <http://purl.org/dc/elements/1.1/format>                                                                                                          |
| Digital Commons Field   | TBD                                                                                                                                                                  |
| Obligation              | Optional                                                                                                                                                             |
| Displayed               | Yes                                                                                                                                                                  |
| Repeatable              | Yes                                                                                                                                                                  |
| Syntax/Formatting       | Do not abbreviate "pages" or "volumes", etc., but do abbreviate units of measurement                                                                                 |
| Controlled Vocabularies | _n/a_                                                                                                                                                                |
| How to Use              | Describe the size and/or duration of the resource, transcribing from the resource itself if possible                                                                 |
| Best Practices          | Follow RDA and/or DCRM guidelines                                                                                                                                    |
| Examples                | Bust: 109.2 cm / 43 in.<br/>Waist: 80 cm / 31.5 in.<br/>Hem: 320 cm / 126 in.<br/>Length (skirt front): 180 cm / 42.5 in.<br/>Length (skirt back): 144.8 cm / 57 in. |

| Label                   | Period of Relevance                                                                                                                                                                                                                                                                                                                       |
| ----------------------- | ----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------- |
| Definition              | Period of Relevance, more commonly called "temporal coverage", refers to the date(s) the resource is _about_.                                                                                                                                                                                                                             |
| Dublin Core mapping     | dc.coverage.temporal ; <http://purl.org/dc/elements/1.1/coverage>                                                                                                                                                                                                                                                                         |
| Digital Commons Field   | TBD                                                                                                                                                                                                                                                                                                                                       |
| Obligation              | Optional                                                                                                                                                                                                                                                                                                                                  |
| Displayed               | Yes                                                                                                                                                                                                                                                                                                                                       |
| Repeatable              | No                                                                                                                                                                                                                                                                                                                                        |
| Syntax/Formatting       | If using numbered dates, the [ISO 8601](https://www.iso.org/iso-8601-date-and-time-format.html) format is preferred. However, this field is not limited to YYYY-MM-DD format. If the date is uncertain, circa and similar indicators are allowed. If indicating a date range, start dates and end dates are separated by an em dash '--'. |
| Controlled Vocabularies | _n/a_                                                                                                                                                                                                                                                                                                                                     |
| How to Use              | Describe the period of time the resource is about, or that is relevant                                                                                                                                                                                                                                                                    |
| Best Practices          | _n/a_                                                                                                                                                                                                                                                                                                                                     |
| Examples                | An annual town report published in 1993 but about the 1992-1993 fiscal year would be:<br />1992-07-01/1993-06-30                                                                                                                                                                                                                          |

| Label                   | Rights Holder                                                                                         |
| ----------------------- | ----------------------------------------------------------------------------------------------------- |
| Definition              | The person or organization who owns or manages the copyright of the resource                          |
| Dublin Core mapping     | dcterms.rightsHolder ; <http://purl.org/dc/terms/rightsHolder>                                        |
| Digital Commons Field   | TBD                                                                                                   |
| Obligation              | Optional                                                                                              |
| Displayed               | Yes                                                                                                   |
| Repeatable              | No                                                                                                    |
| Syntax/Formatting       | _n/a_                                                                                                 |
| Controlled Vocabularies | _n/a_                                                                                                 |
| How to Use              | Transcribe the information (usually in a copyright statement) directly from resource or version known |
| Best Practices          | _n/a_                                                                                                 |
| Examples                | Dimond Library, University of New Hampshire                                                           |

| Label                   | Scanning Information                                                          |
| ----------------------- | ----------------------------------------------------------------------------- |
| Definition              | The details of who scanned the resource, etc.                                 |
| Dublin Core mapping     | dcterms.contributor ; <http://purl.org/dc/terms/contributor>                  |
| Digital Commons Field   | TBD                                                                           |
| Obligation              | Optional                                                                      |
| Displayed               | Yes                                                                           |
| Repeatable              | Yes                                                                           |
| Syntax/Formatting       | _n/a_                                                                         |
| Controlled Vocabularies | _n/a_                                                                         |
| How to Use              | Describe the scanning information using Digital Collections standard practice |
| Best Practices          | If needed/desired, scanning information can go into Comments fields           |
| Examples                | Scanned by Internet Archive, Open Content Alliance (2008)                     |

| Label                   | Source                                                                                                                                                      |
| ----------------------- | ----------------------------------------------------------------------------------------------------------------------------------------------------------- |
| Definition              | The original item or location or the resource                                                                                                               |
| Dublin Core mapping     | dc.source ; <http://purl.org/dc/elements/1.1/source>                                                                                                        |
| Digital Commons Field   | TBD                                                                                                                                                         |
| Obligation              | Optional                                                                                                                                                    |
| Displayed               | Yes                                                                                                                                                         |
| Repeatable              | Yes                                                                                                                                                         |
| Syntax/Formatting       | _n/a_                                                                                                                                                       |
| Controlled Vocabularies | _n/a_                                                                                                                                                       |
| How to Use              | Describe where the original item is from (or where it can be linked from now). If the item is in a finding aid or comes from external sources, link it here |
| Best Practices          | Use a URI/URL when possible<br/>Repeat this field if you give more than one source/form of the source                                                       |
| Examples                | <https://www.library.unh.edu/find/archives/collections/henderson-n-white-sheet-music-collection-1902-1905>                                                  |
