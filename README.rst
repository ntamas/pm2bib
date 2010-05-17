============================================
pm2bib: import PubMed references into BibTeX
============================================

:Author: Tamás Nepusz
:Email: ntamas@gmail.com

This is a simple Python module that can import references into a BibTeX
bibliography based on PubMed IDs. It is based on pyP2B_, the excellent work
of Jean-Etienne Poirrier (see his contact info on his webpage). I did
some refactoring, implemented the escaping of capital letters in the
**Title** field, removed the GUI parts and added support for non-numeric
values in the **Number** field.

.. _pyP2B: http://www.poirrier.be/~jean-etienne/software/pyp2b/

Usage
-----

Command-line usage is dead simple. Assuming that you have put the script
somewhere in your path (and you are not using Windows), you can run the
script as follows::

  $ pm2bib 20214776

This will output a nicely formatted BibTeX snippet for the paper with
PubMed ID 20214776. If you have your bibliography in a file called
``biblio.bib``, you can simply append the output of ``pm2bib``
directly::

  $ pm2bib 20214776 >>biblio.bib

Alternatively, if you are using ``vim`` (like I do) and you quickly
want to import a paper into your bibliography, open up ``biblio.bib``
in ``vim`` and type ``:r! pm2bib 20214776`` to insert the output of
``pm2bib`` directly into the current buffer.

Bugs
----

Nothing is perfect. If you happen to find a bug in ``pm2bib``, send
me a message to the email address above.
