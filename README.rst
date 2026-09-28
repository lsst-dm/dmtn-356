.. image:: https://img.shields.io/badge/dmtn--356-lsst.io-brightgreen.svg
   :target: https://dmtn-356.lsst.io
.. image:: https://github.com/lsst-dm/dmtn-356/workflows/CI/badge.svg
   :target: https://github.com/lsst-dm/dmtn-356/actions/

######################################################################################
From Petabytes to Discovery: The Computing Ecosystem Powering Rubin Observatory's LSST
######################################################################################

DMTN-356
========

The Vera C. Rubin Observatory began the Legacy Survey of Space and Time (LSST), a ten-year optical survey of the southern sky, on 30 June 2026. This paper presents early Rubin images and discoveries, focusing on the data management system that makes science at this scale possible. Building on  LHC-scale distributed computing experience, Rubin deploys HEP tools, including Rucio and  CernVM-FS for large-scale data distribution and workflow management at its three data facilities: SLAC, an ATLAS Tier-2 site, and the French and UK facilities, both long-standing LHC Tier-1 centres. We describe the end-to-end Rubin computing ecosystem and lessons from this cross-disciplinary collaboration for  future data-intensive experiments.

Links
=====

- Live drafts: https://dmtn-356.lsst.io
- GitHub: https://github.com/lsst-dm/dmtn-356

Build
=====

This repository includes lsst-texmf_ as a Git submodule.
Clone this repository::

    git clone --recurse-submodules https://github.com/lsst-dm/dmtn-356

Compile the PDF::

    make

Clean built files::

    make clean

Updating acronyms
-----------------

A table of the technote's acronyms and their definitions are maintained in the `acronyms.tex` file, which is committed as part of this repository.
To update the acronyms table in ``acronyms.tex``::

    make acronyms.tex

*Note: this command requires that this repository was cloned as a submodule.*

The acronyms discovery code scans the LaTeX source for probable acronyms.
You can ensure that certain strings aren't treated as acronyms by adding them to the `skipacronyms.txt <./skipacronyms.txt>`_ file.

The lsst-texmf_ repository centrally maintains definitions for LSST acronyms.
You can also add new acronym definitions, or override the definitions of acronyms, by editing the `myacronyms.txt <./myacronyms.txt>`_ file.

Updating lsst-texmf
-------------------

`lsst-texmf`_ includes BibTeX files, the ``lsstdoc`` class file, and acronym definitions, among other essential tooling for LSST's LaTeX documentation projects.
To update to a newer version of `lsst-texmf`_, you can update the submodule in this repository::

   git submodule update --init --recursive

Commit, then push, the updated submodule.

.. _lsst-texmf: https://github.com/lsst/lsst-texmf

Publication Right Form
======================

All authors must sign the `Web of Conferences Publication Right Form`_ before the paper can be published.
Download, complete, and return the form to the conference editors.

.. _Web of Conferences Publication Right Form: https://www.webofconferences.org/doc_journal/woc/publication_right_form.pdf
