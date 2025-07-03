
# A quarto template for MPDI journal articles

This quarto template is designed to create LaTeX files that can be submitted to
MDPI journals following their [Information for Authors](https://www.mdpi.com/authors).
This template is not officially supported or endorsed by MDPI.  If you encounter
any difficulties or discover edge cases not supported by this template, please submit
an issue on GitHub.

## Creating a New Article

To create a new article using this format:

```bash
quarto use template rpruim/mdpi
```

This will create a new directory with an example document that uses this format.

## Using with an Existing Document

To add this format to an existing document:

```bash
quarto add rpruim/mdpi
```

Then, add the format to your document options:

```yaml
format:
  mdpi-pdf: 
    keep-tex: true
```    

This will allow you to render an article to PDF but retain the `.tex` file for submission to
an MDPI journal.

## Additional YAML Options

### LaTeX package options

The mdpi LaTeX package uses a number of package options to specify things 
like the journal to which a paper is being submitted. These can be specified 
using `classoption` in the YAML header, as is shown in the template document.

```yaml
format: 
  mdpi-pdf:
    classoption: [energies,article,submit,pdflatex,moreauthors]
    pdf-engine: pdflatex
```

Here is the documentation from the MDPI template LaTeX file regarding the available
options.

```

%--------------------
% Class Options:
%--------------------
%----------
% journal
%----------
% Choose between the following MDPI journals:
% accountaudit, acoustics, actuators, addictions, adhesives, admsci,
% adolescents, aerobiology, aerospace, agriculture, agriengineering,
% agrochemicals, agronomy, ai, air, algorithms, allergies, alloys, amh, analytica,
% analytics, anatomia, anesthres, animals, antibiotics, antibodies, antioxidants,
% applbiosci, appliedchem, appliedmath, appliedphys, applmech, applmicrobiol,
% applnano, applsci, aquacj, architecture, arm, arthropoda, arts, asc, asi,
% astronomy, atmosphere, atoms, audiolres, automation, axioms, bacteria,
% batteries, bdcc, behavsci, beverages, biochem, bioengineering, biologics,
% biology, biomass, biomechanics, biomed, biomedicines, biomedinformatics,
% biomimetics, biomolecules, biophysica, biosensors, biosphere, biotech, birds,
% blockchains, bloods, blsf, brainsci, breath, buildings, businesses, cancers,
% carbon, cardiogenetics, catalysts, cells, ceramics, challenges, chemengineering,
% chemistry, chemosensors, chemproc, children, chips, cimb, civileng,
% cleantechnol, climate, clinbioenerg, clinpract, clockssleep, cmd, cmtr, coasts,
% coatings, colloids, colorants, commodities, complications, compounds,
% computation, computers, condensedmatter, conservation, constrmater, cosmetics,
% covid, crops, cryo, cryptography, crystals, csmf, ctn, curroncol, cyber, dairy,
% data, ddc, dentistry, dermato, dermatopathology, designs, devices, diabetology,
% diagnostics, dietetics, digital, disabilities, diseases, diversity, dna, drones,
% dynamics, earth, ebj, ecm, ecologies, econometrics, economies, education, eesp,
% ejihpe, electricity, electrochem, electronicmat, electronics, encyclopedia,
% endocrines, energies, eng, engproc, ent, entomology, entropy, environments,
% epidemiologia, epigenomes, esa, est, famsci, fermentation, fibers, fintech,
% fire, fishes, fluids, foods, forecasting, forensicsci, forests, fossstud,
% foundations, fractalfract, fuels, future, futureinternet, futureparasites,
% futurepharmacol, futurephys, futuretransp, galaxies, games, gases, gastroent,
% gastrointestdisord, gastronomy, gels, genealogy, genes, geographies, geohazards,
% geomatics, geometry, geosciences, geotechnics, geriatrics, glacies, grasses,
% greenhealth, gucdd, hardware, hazardousmatters, healthcare, hearts, hemato,
% hematolrep, heritage, higheredu, highthroughput, histories, horticulturae,
% hospitals, humanities, humans, hydrobiology, hydrogen, hydrology, hygiene, idr,
% iic, ijerph, ijfs, ijgi, ijmd, ijms, ijns, ijpb, ijt, ijtm, ijtpp, ime, immuno,
% informatics, information, infrastructures, inorganics, insects, instruments,
% inventions, iot, j, jal, jcdd, jcm, jcp, jcs, jcto, jdad, jdb, jeta, jfb, jfmk,
% jimaging, jintelligence, jlpea, jmahp, jmmp, jmms, jmp, jmse, jne, jnt, jof,
% joitmc, joma, jop, jor, journalmedia, jox, jpbi, jpm, jrfm, jsan, jtaer, jvd,
% jzbg, kidney, kidneydial, kinasesphosphatases, knowledge, labmed, laboratories,
% land, languages, laws, life, lights, limnolrev, lipidology, liquids, literature,
% livers, logics, logistics, lubricants, lymphatics, machines, macromol,
% magnetism, magnetochemistry, make, marinedrugs, materials, materproc,
% mathematics, mca, measurements, medicina, medicines, medsci, membranes, merits,
% metabolites, metals, meteorology, methane, metrics, metrology, micro,
% microarrays, microbiolres, microelectronics, micromachines, microorganisms,
% microplastics, microwave, minerals, mining, mmphys, modelling, molbank,
% molecules, mps, msf, mti, multimedia, muscles, nanoenergyadv, nanomanufacturing,
% nanomaterials, ncrna, ndt, network, neuroglia, neurolint, neurosci, nitrogen,
% notspecified, nursrep, nutraceuticals, nutrients, obesities, oceans, ohbm, onco,
% oncopathology, optics, oral, organics, organoids, osteology, oxygen, parasites,
% parasitologia, particles, pathogens, pathophysiology, pediatrrep, pets,
% pharmaceuticals, pharmaceutics, pharmacoepidemiology, pharmacy, philosophies,
% photochem, photonics, phycology, physchem, physics, physiologia, plants, plasma,
% platforms, pollutants, polymers, polysaccharides, populations, poultry, powders,
% preprints, proceedings, processes, prosthesis, proteomes, psf, psych,
% psychiatryint, psychoactives, psycholint, publications, purification,
% quantumrep, quaternary, qubs, radiation, reactions, realestate, receptors,
% recycling, regeneration, religions, remotesensing, reports, reprodmed,
% resources, rheumato, risks, robotics, rsee, ruminants, safety, sci, scipharm,
% sclerosis, seeds, sensors, separations, sexes, signals, sinusitis, siuj, skins,
% smartcities, sna, societies, socsci, software, soilsystems, solar, solids,
% spectroscj, sports, standards, stats, std, stresses, surfaces, surgeries,
% suschem, sustainability, symmetry, synbio, systems, tae, targets, taxonomy,
% technologies, telecom, test, textiles, thalassrep, therapeutics, thermo,
% timespace, tomography, tourismhosp, toxics, toxins, transplantology,
% transportation, traumacare, traumas, tropicalmed, universe, urbansci, uro,
% vaccines, vehicles, venereology, vetsci, vibration, virtualworlds, viruses,
% vision, waste, water, wem, wevj, wild, wind, women, world, youth, zoonoticdis
% 
%---------
% article
%---------
% The default type of manuscript is "article", but can be replaced by:
% abstract, addendum, article, benchmark, book, bookreview, briefcommunication,
% briefreport, casereport, changes, clinicopathologicalchallenge, comment,
% commentary, communication, conceptpaper, conferenceproceedings, correction,
% conferencereport, creative, datadescriptor, discussion, entry,
% expressionofconcern, extendedabstract, editorial, essay, erratum, fieldguide,
% hypothesis, interestingimages, letter, meetingreport, monograph,
% newbookreceived, obituary, opinion, proceedingpaper, projectreport, reply,
% retraction, review, perspective, protocol, shortnote, studyprotocol, supfile,
% systematicreview, technicalnote, viewpoint, guidelines, registeredreport,
% tutorial,  giantsinurology, urologyaroundtheworld
% supfile = supplementary materials

%----------
% submit
%----------
% The class option "submit" will be changed to "accept" by the Editorial Office
% when the paper is accepted. This will only make changes to the frontpage (e.g.,
% the logo of the journal will get visible), the headings, and the copyright
% information. Also, line numbering will be removed. Journal info and pagination
% for accepted papers will also be assigned by the Editorial Office.

%------------------
% moreauthors
%------------------
% If there is only one author the class option oneauthor should be used.
% Otherwise use the class option moreauthors.

%---------
% pdftex
%---------
% The option pdftex is for use with pdfLaTeX. Remove "pdftex" for (1) compiling
% with LaTeX & dvi2pdf (if eps figures are used) or for (2) compiling with
% XeLaTeX.
```


### Authors

Quarto provides a rich set of YAML metadata keys to describe authors and their affiliations.
If you provide this information, the mdpi quarto template will do its best to use that 
information in preparing your document.

Unfortunately, the mdpi LaTeX package has a fairly brittle way of dealing with author 
information. If you want to fully comply with their design, you will probably need 
to provide the information as a LaTeX file specified by `author-block` in the YAML.
If this exists, it will be used in place of any code generated from the `author` section
of the YAML.

See the template and its accompanying `author-info.tex` for examples.

## Example

Here is the source code for a sample document: [template.qmd](template.qmd).
