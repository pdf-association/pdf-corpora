# **PDF Corpora**

![LinkedIn](https://img.shields.io/static/v1?style=social&label=LinkedIn&logo=linkedin&message=PDF-Association)
&nbsp;&nbsp;&nbsp;
![Twitter Follow](https://img.shields.io/twitter/follow/PDFAssociation?style=social)
&nbsp;&nbsp;&nbsp;
![YouTube Channel Subscribers](https://img.shields.io/youtube/channel/subscribers/UCJL_M0VH2lm65gvGVarUTKQ?style=social)

This index references a number of the more significant public corpora (data sets) that may contain both valid and invalid, real and synthetic PDF files, reflecting the realities of processing PDF files 'from the wild'. In addition, targeted test suites for specific PDF features or ISO subsets of PDF are also listed. It is not intended to be a list of every website where PDFs may be obtained.

This informative resource is freely provided to all interested PDF developers, end-users and researchers. It does not reflect an endorsement of any organization, website or corpus. If you currate, maintain or identify other corpora that you believe might be useful to the PDF industry and is freely available please contact us. Some corpora may require registration in order to access.


**CAUTION: like any file downloaded from the internet, good computer security and hygiene practices should always be employed as some of these corpora contain files that are malicious! Use at your own risk!**

For groups interested in creating their own PDF-centric corpora using [GitHub](https://github.com/), please consider using [Git LFS](https://git-lfs.github.com/) so that large files can be easily supported.

## CC-MAIN-2021-31-PDF-UNTRUNCATED (SafeDocs)

- https://digitalcorpora.org/cc-main-2021-31-pdf-untruncated/
- https://downloads.digitalcorpora.org/corpora/files/CC-MAIN-2021-31-PDF-UNTRUNCATED/

Announced in May 2023, this corpus contains nearly 8 million PDFs gathered from across the web in July/August of 2021. The PDF files were initially identified by [Common Crawl](https://commoncrawl.org/) as part of their July/August 2021 crawl (identified as "CC-MAIN-2021-31") with all truncated PDFs (those >1MB) subsequently updated and collated as part of the DARPA SafeDocs program. As far as we know this is the largest corpus of PDFs that is an unbiased representative of the current global public web, overcoming truncation limitations, top-level domain constraints or other limitations that prior web-crawled corpora impose. See https://pdfa.org/new-large-scale-pdf-corpus-now-publicly-available/ for a more detailed description. 


## UNSAFE-DOCS (CC-MAIN-2021-31-UNSAFE) (SafeDocs)

- https://digitalcorpora.org/corpora/file-corpora/unsafe-docs-cc-main-2021-31-unsafe/
- https://pdfa.org/unsafe-docs-a-new-safedocs-corpus-including-the-voice-of-the-offense/ (_announcement_)

**CAUTION: this dataset is known to contain malformed and malicious PDF files that impact various PDF processors!** 

"_Following the release of the curated CC-MAIN-2021-31-PDF-UNTRUNCATED corpus, the UNSAFE-DOCS corpus contains over 5.0 million files collected by a team at NASA’s Jet Propulsion Laboratory (JPL) or synthetically generated by Kudu Dynamics ‘ “Voice of the Offense” (VoO) team for the Defense Advanced Research Project Agency (DARPA)’s SafeDocs Program.
The common-crawl component of the UNSAFE-DOCS corpus (over 3.9 million PDF files as collected by a team at NASA’s Jet Propulsion Laboratory (JPL)) includes some truncated PDF files, as described in the paper “Building a Wide Reach Corpus for Secure Parser Development” by Allison et al ([[slides](http://spw20.langsec.org/slides/corpus_LangSec2020.pdf)] [[paper](http://spw20.langsec.org/papers/corpus_LangSec2020.pdf)]). This component was utilized within the SafeDocs program as the starting point for many generated files and as the Program’s evaluation corpus. It was later expanded and improved to become CC-MAIN-2021-31-PDF-UNTRUNCATED._"

## GovDocs1
- https://digitalcorpora.org/corpora/files

This is a very well-studied and large corpus created in 2010, comprising almost 1 million documents from the USA .gov TLD, of which more than 231,000 are PDF documents. The above URL provides lots of detailed information and references. For reference, the 1000 ZIP files total about 308GB. As of November 2020, GovDocs1 has joined the AWS Open Data Sponsorship Program and data is now available directly in AWS S3 (see https://digitalcorpora.org/s3_browser.html#corpora/files/govdocs1/zipfiles/)


## CommonCrawl.org
- http://commoncrawl.org/

The Common Crawl corpus contains petabytes of data collected since 2008 and is the core data behind the Wayback Machine (https://web.archive.org/). It contains raw web page data, extracted metadata and text extractions and, of course, millions and millions of PDF files gathered from across the web.

NOTE: Based on published SafeDocs research, many PDFs in the CommonCrawl database are known to be truncated. See: T. Allison et al., “*Building a Wide Reach Corpus*,” in LangSec 2020, May 2020. http://spw20.langsec.org/papers/corpus_LangSec2020.pdf:

> Common Crawl truncates files at 1 MB. If researchers require intact files, they must re-pull truncated files from the original websites. In the December, 2019 crawl, nearly 430,000 PDFs (22%) were truncated.


## SafeDocs "Issue Tracker" Corpus
- Individual PDFs can be downloaded from the Apache Tika regression test server: https://corpora.tika.apache.org/base/docs/bug_trackers/
- The November 2020 update conveniently pre-packages all PDFs into six compressed tarballs (.tgz files): https://corpora.tika.apache.org/base/packaged/pdfs/
- The initial release from Sept 2020 is also still available from https://corpora.tika.apache.org/base/packaged/pdfs/archive/

An outcome of the DARPA-funded SafeDocs research program, a large and growing corpus (>32K files, >31GB) collated by targeted deep-crawls of various issue trackers (e.g. Bugzilla, JIRA, GitHub) to extract PDF attachments on public bug reports for various well-known open-source PDF-aware implementations. These PDFs are not directly discoverable via standard internet search engines. By its very nature, this corpus has a higher-than-normal quantity of unusual and malformed PDFs. Further technical details of this corpus can be found at https://www.pdfa.org/a-new-stressful-pdf-corpus/ and https://www.pdfa.org/stressful-pdf-corpus-grows/ as well as README files on the Apache Tika regression server.

**NOTE: this unsanitized collated corpus contains a few PDFs that are known to trigger certain anti-malware/anti-virus programs.**

## Library of Congress 1000 .gov dataset

- https://www.loc.gov/item/2020445568/

Effectively a smaller but updated dataset, similar to GovDocs1: "_This dataset of 1,000 PDF files was generated from indexes of the Web archives, which were used to derive a random list of 1,000 items identified as PDF files and hosted on .gov domains. The set includes 1,000 unique PDF files and minimal metadata about these PDFs, including links to their locations within the Library's web archive. Dataset originally created 11/6/2018_."

## FoxHex0ne Mutations
- https://foxhex0ne.com/

A set of mutated PDFs (and other document formats) created via mutation-based fuzzing. See also ~http://foxhex0ne.blogspot.com/2020/01/lets-continue-with-corpus-distillation.html~ https://web.archive.org/web/20200325183758/http://foxhex0ne.blogspot.com/2020/01/lets-continue-with-corpus-distillation.html.


## OpenPreserve Foundation Format Corpus
- https://github.com/openpreserve/format-corpus

This is a digital preservation-focused corpus that is openly licensed and covers a wide range of formats and creation tools.


## The Archivist's PDF Cabinet of Horrors
- https://github.com/openpreserve/format-corpus/tree/master/pdfCabinetOfHorrors

A smaller sub-corpus of PDF test files, created for detecting PDF features that are generally undesirable in an archival setting.


## Cal Poly Graphic Communications PDF/VT Test File Suite 1.0.1
- https://www.pdfa.org/resource/cal-poly-pdfvt-test-suite/

This suite provides a collection of four sets of graphically-rich, robust and valid ISO 16612-2 PDF/VT-1 files targeting high-volume variable data printing. Each set comprises PDFs with 10, 100, 500, 1000, 5000, 10000, and 15000 records and can be useful for examining how PDF technology scales as PDF file size and page counts increase.


## VeraPDF Test Suite for PDF/A
- https://www.pdfa.org/resource/verapdf-test-suite/
- https://github.com/veraPDF/veraPDF-corpus

The veraPDF test corpus targets the ISO 19005 family of PDF/A specifications (Versions 1B, 1A, 2B, 2U, 2A, 3B, 3U, 3A) as well as a number of additional PDF test files for ISO 32000-1:2008 (PDF 1.7). This test suite complements the Isartor and Bavaria PDF/A-1b test suites and follows their test file pattern:
 - all test files are atomic;
 - they are self-documented via the document outlines; and
 - the naming pattern and the directory structure indicate relevant parts of ISO 19005 specifications

## Isartor Test Suite for PDF/A-1b
- https://www.pdfa.org/resource/isartor-test-suite/

This test suite comprises a set of files that are used to check the conformance with PDF/A-1. More precisely, the Isartor test suite can be used to "validate the validators": It deliberately violates the requirements of PDF/A-1 in a systematic way in order to check whether PDF/A-1 validation software actually finds the violations.


## BFO PDF/A Test Suite
- https://github.com/bfosupport/pdfa-testsuite

A collection of about 40 PDF documents that should either pass or fail a conformance test against the specified ISO 19005 PDF/A profile. The description.txt file lists the reason they should pass or fail. This collection was inspired by the Isartor test suite and follows a similar layout with respect to test case names, including the section of the PDF/A specification to which each test refers. Unlike Isartor there are also  valid documents that test a particular area of the specification.


## "Synthetic PDF Testset for File Format Validation"
- https://www.radar-service.eu/radar/en/dataset/JtlOdwQquZWDqQdq

(Abstract) "_This data set presents a corpus of light-weight files designed to test the validation criteria of JHOVE's PDF module against "well-formedness". Test cases are based on structural requirements for PDF files as per ISO 32000-1:2008 standard. The basis for all test files is a single page, one line document with no special features such as linearization. While such a light-weight document only allows to check against a fragment of standard requirements, the focus was put on basic structure violations at the header, trailer, document catalog, page tree node and cross-reference levels. The test set also checks for basic violations at the page node, page resource and stream object level. The accompanying spreadsheet briefly categorizes and describes the test set and includes the outcome when running the test set against JHOVE 1.16, PDF-hul 1.8 as well as Adobe Acrobat Professional XI Pro (11.0.15). The spreadsheet also includes a codecov coverage statistic for the test set in relation to the JHOVE 1.16, PDF-hul 1.8 module. Further information can be found in the paper "A PDF Test-Set for Well-Formedness Validation in JHOVE - The Good, the Bad and the Ugly", published in the proceedings of the 14th International Conference on Digital Preservation (Kyoto, Japan, September 25-29 2017). While the spreadsheet only contains results of running the test set against JHOVE, it can be used as a ground truth for any file format validation process._"

## Ghent Working Group (GWG) Output Test Suite
- https://www.gwg.org/workflow-tools-downloads/test-suites/ghent-output-suite/

The Ghent Output Suite (currently v5.0) has been created for testing PDF processing in the graphic arts industry and to determine whether workflows are behaving as expected according to the ISO 15930 family of PDF/X standards. The PDF files provide a series of test patches that can be used by end users of graphic arts equipment as well as developers of applications that handle PDF files. This test suite is highly technical and a good understanding of ISO 15930 is essential.


## PDF/UA Reference Suite
- https://www.pdfa.org/resource/pdfua-reference-suite/

To serve as a reference for software developers and practitioners interested in best practices for creating tagged and accessible PDF files, the PDF Association's PDF/UA Competence Center has posted a set of 10 PDF documents conforming to ISO 14289-1 PDF/UA-1.


## Matterhorn Protocol 1.02
- https://www.pdfa.org/resource/the-matterhorn-protocol-1-02/

 The PDF Association's PDF/UA Competence Center developed the Matterhorn Protocol as a list of all the possible ways to fail PDF/UA. Following the requirements of PDF/UA, the document consists of 31 checkpoints comprised of 136 Failure Conditions. The Matterhorn Protocol 1.02 (PDF, 339kB, 2014-06-26) is delivered as a PDF file conforming to PDF/UA-1 (ISO 14289-1) and to PDF/A-2a (ISO 19005-2) and is a reference-quality PDF/UA file.


## Altona Test Suite
- http://www.eci.org/en/downloads

The Altona Test Suite is a set of highly technical PDF files and patches specifically designed for testing ISO 15930 PDF/X compliance and color accuracy including transparency blending, font handling, smooth shades, gray balance, overprinting, etc.


## 3D PDF Showcase
- https://www.pdfa.org/3d-pdf-showcase/

Originally collated by members of the 3D PDF Consortium ([Wayback Machine link](https://web.archive.org/web/20220425214456/http://3dpdfconsortium.org/showcase/)), the 3D PDF showcase corpus provides about 20 PDFs containing different kinds of 3D content from various creators. All PDFs were transitioned to the PDF Association.


## Google pdfium Regression Test Suite
- https://pdfium.googlesource.com/pdfium_tests/

A set of PDFs (both real and synthetic) used in regression testing Google's pdfium implementation used in Chrome and elsewhere.


## Mozilla pdf.js Regression Test Suite
- https://github.com/mozilla/pdf.js/tree/master/test/pdfs

PDF.js is a PDF viewer supported by Mozilla that is built with HTML5.


## Ghent Working Group (GWG) Processing Steps
- https://www.gwg.org/processing-steps-specification/

Three sample PDF files containing ISO 19593-1 compliant processing step data (i.e. PDF optional content layers describing cut contours (die lines), varnish, braille, legends, etc.). These sample files are fully compliant with the ISO standard and serve to illustrate the concepts discussed in the standard.


## iText Regression Test Suite
- https://github.com/itext/itext7

Among the iText Java source code is a sizeable corpus of just under 4,000 PDF files provided as the regression test suite for the iText PDF library. The PDF files  are nicely classified as to the PDF feature being tested, including a [good suite of encrypted PDFs](https://github.com/itext/itext7/tree/develop/kernel/src/test/resources/com/itextpdf/kernel/crypto/PdfEncryptionTest) and many others. Each PDF tends to be nice and small for targetted testing of a specific feature with set permutations of PDF keys, values, etc.  

## Asymptote gallery samples
- https://asymptote.sourceforge.io/gallery/PDFs/index.html: advanced shadings, clips, etc. 
- https://asymptote.sourceforge.io/gallery/animations/index.html: various PDFs containing embedded movies

Asymptote is an open-source vector graphics language with advanced rendering capabilities. It can output to PDF using many of the  advanced PDF graphics capabilities such as complex shadings/patterns, complex clips, etc. (rather than dumbing down to pre-rendered bitmap images like other packages). The Asymptote Gallery provides many examples in PDF format.

## Legacy Adobe Acrobat and Reader Engineering team test files (via Wayback Machine)
- https://web.archive.org/web/20130503115947/http://acroeng.adobe.com/wp/
- https://web.archive.org/web/20130717074145/http://acroeng.adobe.com/wp/?page_id=208

Note: all data is from the Wayback Machine and many of the PDFs were not archived. Sometimes files of the same name and size can be located elsewhere on the internet. 

Various small test sets (such as "Fast Web View/Linearization", "PDF Page Elements", "PDF Files Elements", "Acrobat Sanity Testing", "PDFs in Browser Testing", "Viewer Testing", and "(ISO) PDF Standards Testing") from the Adobe engineering teams responsible for Adobe Reader and Acrobat.

## Ground-truthed data sets for PDF table recognition
- http://www.tamirhassan.com/html/dataset.html

Two ground-truthed datasets of natively-digital PDF documents containing tables. These documents have been collected systematically from the European Union and US Government websites.


## PDF-TREX Table Recognition and Extraction data set
- http://staff.icar.cnr.it/ruffolo/pdf-trex

The freely available PDF-TREX dataset is a standard dataset in the TREX (Table Recognition and EXtraction) field. The dataset contains 100 PDF documents and 164 tables having different layouts.


##  US National Library of Medicine - National Institutes of Health
- https://www.ncbi.nlm.nih.gov/pmc/tools/openftlist/

A collection of scientific PDF publications is included in the PubMed Central Open Access Subset (commercial use collection).


## US Incident Management Situation Reports from 1990 to 2022

- https://famprod.nwcg.gov/batchout/IMSRS_from_1990_to_2022/
- https://www.nature.com/articles/s41597-023-02876-8 (_article_)

 Dataset of Incident Management Situation Reports (IMSR) from 1990 to 2022, which document daily wildland fire situations across ten geographical regions in the United States.
 
## NEPATEC1.0 - US Environmental Impact Statement (EIS) PDF dataset

- Sharma, S. et al. (2024) ‘NEPATEC1.0: First Large-Scale Text Corpus of National Environmental Policy Act PDF Documents’, p. 7. https://www.pnnl.gov/sites/default/files/media/file/PNNL_PolicyAI_Dataset_Model_Release_IR_06_26.pdf.
- https://huggingface.co/datasets/PolicyAI/NEPATEC1.0 

"_NEPATEC1.0 is an AI-ready dataset that contains data extracted from the Environmental Impact
Statement (EIS) Database provided by U.S. Environmental Protection Agency (EPA). An EIS is a
government document that analyzes the potential environmental effects of a proposed project and
identifies ways to mitigate those effects. NEPATEC1.0 contains textual data and associated metadata
extracted from 2,917 projects. These projects contain 28,212 documents, 4.6 million pages, and over
3.6 billion tokens of textual data (using GPT2 tokenizer)._"


## OpenLibrary.org
- https://openlibrary.org/

Scanned books and other publications can be downloaded in PDF format. Note that many such PDFs are quite large in size.


## International Labour Organization
- https://www.ilo.org/public/libdoc/ilo/ILO-SR/

This is a corpus of approximately 730 legacy PDF documents (from 2008-), however it has somewhat limited variability in PDF technical and syntactic constructs.


## New York State Regents Exams 

- https://www.nysl.nysed.gov/regentsexams.htm (overview)
- https://nysl.ptfs.com/knowvation/app/consolidatedSearch/#search/v=list,c=1,sm=s,l=library1_lib%2Clibrary4_lib%2Clibrary5_lib (Search page)

"_NYS Regents Exams in PDF format are part of the Library's Digital Collections. In addition to current exams, many historical ones have also been digitized: some of the oldest Regents Exams currently available online are in Physical Geography (1884) and Astronomy (1893)._". See https://www.nysl.nysed.gov/collections/regentsexams/ for some images of content. Corpus has a variety of complex content such as music scores, mathematics, etc. 


## Mikal's "pdfdb"

- http://www.stillhq.com/pdfdb/db.html (dead link)
    - Wayback Machine link: https://web.archive.org/web/20190212183538/http://www.stillhq.com/pdfdb/db.html
- https://www.madebymikal.com/pdfdb/db.html (also a dead link)

A database referenced from StackOverflow (https://stackoverflow.com/questions/14386393/pdf-specification-compliance-testing-sample-files) that is no longer directly available.


## Vasulka PDF Archive (history of video and electronic art)
- https://vasulka.org/archive/sitemap.html

From https://vasulka.org/about_archive.html: "_The Vasulka Archive currently consists of over 27,000 pages of documents relevant to the history of video and electronic art. These include articles, essays, interviews, reviews, schematics, diagrams, illustrations, posters, concert programs, photographs, and correspondence. While a large percentage of this material directly relates to the art and careers of Steina and Woody Vasulka, there are well over 200 artists and scholars represented. Some of the material has been taken from periodicals that are both in and out of print. The rest has been taken from the personal collection of the Vasulkas that began over thirty years ago._"


## Artifex MuPDF Public Test Corpus

- http://git.ghostscript.com/?p=tests.git;a=summary

Public test corpus for Ghostscript/MuPDF, maintained by Artifex (https://mupdf.com/).


## Qiqqa's "Evil Base" Test Corpus

- https://github.com/GerHobbelt/Evil-PDF-Library-for-Qiqqa

Test corpus used by the [Qiqqa PDF document management software](https://github.com/jimmejardine/qiqqa-open-source) for testing various PDF-centric processes (metadata extraction, text extraction and OCR for meta-search & ~-research, page rendering/viewing, ...).

**WARNING: Be aware that this corpus includes *malformed*, *invalid* and *malicious* PDFs**, which serve as an acid test for robustness testing production-level PDF processors. *Cave canem.*


## Digital Library of Slovenia

- https://dlib.si/?&language=eng (English website)
- As described in ["_A Lightweight Approach to a Giga-Corpus of Historical Periodicals: The Story of a Slovenian Historical Newspaper Collection_"](https://aclanthology.org/2024.lrec-main.61/) by Filip Dobranić, Bojan Evkoski and Nikola Ljubešić.

The Digital Library of Slovenia includes various kinds of PDF documents, including scans of historic documents with overlaid invisible text (text render mode 3). Many PDFs also include pure text equivalents. It is a useful corpus for non-English Slovac documents. 


## Italian Institute for Environmental Protection and Research (ISPRA) regional snowfall records

- http://www.bio.isprambiente.it/annalipdf/
- Described by the article: ["Historical snowfall precipitation data in the Apennine Mountains, Italy" by Capozzi Vincenzo; Serrapica Francesco; Rocco Armando; Annella Clizia and Budillon Giorgio, 2024-01-01](https://ricerca.uniparthenope.it/handle/11367/133936)

Scans of historical Italian snowfall records by region stored as PDF : "_...  the original data sources of this database, the Hydrological Yearbooks of the NHMS, are freely accessible in printed version (i.e. as scanned images in portable document format) through the Italian Institute for Environmental Protection and Research (ISPRA) website (http://www.bio.isprambiente.it/annalipdf)._"


## IUST-PDFCorpus

- https://zenodo.org/records/3484013
- described in "[Format-aware Learn&Fuzz: Deep Test Data Generation for Efficient Fuzzing](https://arxiv.org/abs/1812.09961v2)"

"_IUST-PDFCorpus is a large set of various PDF files, aimed at building and manipulating new PDF files, to test, debug, and improve the qualification of real-world PDF readers [snip]. IUST-PDFCorpus contains 6,141 PDF complete files in various sizes and contents. The corpus includes 507,299 PDF data objects and 151,132 PDF streams extracted from the set of complete files. Data objects are in the textual format while streams have a binary format and together they make PDF files. In addition, we attached the code coverage of each PDF file when it used as test data in testing MuPDF. The coverage info is available in both binary and XML formats. PDF data objects are organized into three categories. The first category contains all objects in the corpus. Each file in this category holds all PDF objects extracted from one PDF file without any preprocessing. The second category is a dataset made by merging all files in the first category with some preprocessing. The dataset is spilled into train, test and validation set which is useful for using in the machine learning tasks. The third category is the same as the second category but in a smaller size for using in the developing stage of different algorithms. IUST-PDFCorpus is collected from various sources including the Mozilla PDF.js open test corpus, some PDFs which are used in AFL as initial seed, and PDFs gathered from existing e-books, software documents, and public web in different languages. We first introduced IUST-PDFCorpus in our paper “Format-aware learn&fuzz: deep test data generation for efficient fuzzing” where we used it to build an intelligent file format fuzzer, called IUST-DeepFuzz. For the time being, we are gathering other file formats to automate testing of related applications._".

## Public Affairs Layout database (PALdb)

- https://github.com/BiDAlab/PALdb - requires personal registration
- As referenced in Peña et al, "Continuous document layout analysis: Human-in-the-loop AI-based data curation, database, and evaluation in the domain of public affairs", Information Fusion, 2024, ISSN 1566-2535, https://doi.org/10.1016/j.inffus.2024.102398. (https://www.sciencedirect.com/science/article/pii/S1566253524001763)

"_The database was collected from a set of 24 data sources from the Spanish administration and comprises nearly 37,910 documents, 441.3K document pages, 138.1M tokens and 8M layout labels. ... 1M images, 118.7K tables, 14.4K links, and 7.1M text blocks_". Intended use of this dataset is for document layout analysis (DLA).

## Various US Government Corpora

In addition to GovDocs1 mentioned above, the following specialized archives provide
many PDFs (largely in US English) but do not provide pre-packaged ZIP files:

* https://governmentattic.org/

> The US Government Attic "_provides electronic copies of thousands of interesting Federal Government documents obtained under the Freedom of Information Act.  Fascinating historical documents, reports on items in the news, oddities and fun stuff and government bloopers, they're all here._". Files are stored as PDFs with many having redactions. There appears to be no combined download of the entire corpus but the web pages are sufficiently simple to recursively fetch using something like `curl` or `wget`.

* https://www.oversight.gov/

> "_Oversight.gov is a publicly accessible, searchable website containing the latest public reports from Federal Inspectors General who are members of the Council of the Inspectors General on Integrity and Efficiency (CIGIE)._" There appears to be no combined download of the entire corpus.

* https://nsarchive.gwu.edu/digital-national-security-archive

> The Digital National Security Archive (DNSA) "_is an invaluable online collection of more than 100,000 declassified records documenting historic U.S. policy decisions._"

* https://archive.org/details/usfederalcourts

> CourtListener’s RECAP court document archive. "_The documents in this collection are from the US Federal Courts. A large collection come from the federal government's project for Public Access to Court Electronic Records (PACER). The PACER Service Center is the Federal Judiciary's centralized registration, billing, and technical support center for electronic access to U.S. District, Bankruptcy, and Appellate court records. For more information on the RECAP project, visit https://www.recapthelaw.org_"


# Malicious Datasets

**These datasets contain malicious PDFs and should be treated with extreme caution!!**

## Canadian Institute for Cybersecurity "CIC-Evasive-PDFMal2022" dataset

* https://www.unb.ca/cic/datasets/pdfmal-2022.html
* https://www.kaggle.com/datasets/dhoogla/cic-evasive-pdfmal2022

> "_Evasive-PDFMal2022 consists of 10,025 records with 5557 malicious and 4468 benign records that tend to evade the common significant features found in each class. This makes them harder to detect by common learning algorithms. We have collected 11,173 malicious files from Contagio, 20,000 malicious files from VirusTotal, and 9,109 benign files from Contagio_."

# *Other formats*

Internally PDF supports many so-called nested or embedded formats, such as JPEG, JPEG 2000, JBIG2, ICC, OpenType and other font programs, as well as conversion from other formats. Thus sources of corpora in other formats may also be of interest to the broader PDF community. Note that PDF can and does technically limit the scope of what certain nested formats can contain, so **do not** assume that all files in these corpora are valid for nesting inside PDF! Always refer to the latest PDF specification \([ISO 32000-2, PDF 2.0](https://www.pdfa.org/resource/iso-32000-pdf/)) for all technical requirements.

##  PRImA Labs

The University of Salford Pattern Recognition & Image Analysis Research Lab (PRImA) provide many image-based data sets "_ranging from historical books and newspapers to contemporary documents_", that have been "_collected, ground-truthed and organised \[as] a number of datasets which are available for research and/or personal use_".

- https://www.primaresearch.org/

## IEEE DataPort

The IEEE DataPort contains some open access data sets. Although mainly focused on machine learning, many data sets are image-based.

- https://ieee-dataport.org/datasets

## AWS Open Data Program

Both GovDocs1 and CommonCrawl are part of the AWS Open Data Program (see above), but there are also many other data sets (mostly image and video related). Data is stored in AWS S3.

- https://registry.opendata.aws/

## Microsoft Research Open Data

The MSR Open Data datasets provide a convenient UI for selecting datasets based on a format (file type) which includes PDF, docx and png. Datasets are stored in Azure.

- https://msropendata.com/

## Kaggle

[Kaggle](https://www.kaggle.com/) provides various datasets mainly intended for machine learning and AI applications. Some include PDFs:

- Scanned-to-PDF receipts from around the world [https://www.kaggle.com/datasets/jenswalter/receipts](https://www.kaggle.com/datasets/jenswalter/receipts)
- 2400+ Resumes [https://www.kaggle.com/datasets/snehaanbhawal/resume-dataset](https://www.kaggle.com/datasets/snehaanbhawal/resume-dataset)
- arXiv PDF publication dataset (stored in Amazon S3) [https://www.kaggle.com/datasets/Cornell-University/arxiv](https://www.kaggle.com/datasets/Cornell-University/arxiv)

## ICC Profiles

PDF files can contain ICC profiles to provide device-independent definitions for color. As a result, all PDF viewers, PDF renderers and many other PDF processors need to have robust handling of ICC profiles. The following links provide ICC-based corpora that PDF developers may therefore find useful (both valid and invalid ICC profiles):

- the ICC website [color.org](https://color.org/profiles.xalter) has many ICC profiles, including probe profiles which can test correct handling of rendering intents
- [Google's SKIA skcms corpus](https://skia.googlesource.com/skcms/+/refs/heads/main/profiles/) includes many good and bad ICC profiles
- [LitteCMS test bed](https://github.com/mm2/Little-CMS/tree/master/testbed)
- a collection of [monitor ICC profiles](https://tftcentral.co.uk/articles/icc_profiles.htm)

# *Legal*
In accordance with Title 17 U.S.C. Section 107, the material in this document is distributed without profit to those who have an interest in understanding the interoperability of PDF files, including for research and educational purposes. If you wish to use the copyrighted material of others that is referenced in this document for purposes of your own that go beyond 'fair use', it is your responsibility to obtain permission from the relevant copyright owner.

The PDF Association does not warrant the accuracy, timeliness or completeness of the information contained in this document. All copyright and trademarks remain with their respective owners. If you have a particular complaint about something you’ve read here, please contact us.
