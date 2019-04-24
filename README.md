# rap-paraphaser
Service to paraphrase the text in the semantic field of turnips with the addition of Russian rap slang


If you want to run a project on a localhost, you will need to follow these steps.
You need the folder site/www:
1. Rename cgi folder to cgi-bin
2. Transfer cgi-bin to www
3. Install additional modules for python - gensim, pymorphy2
4. Check that in index.html (located in www) on 48 and 49 lines of the link are spelled as "cgi-bin / ..."
5. You come into cgi-bin, now identical changes for rephrase.py, associate.py:
Find the line model = gensim ... (datapath ("muam.nikhost -....... / model.bin"))
6. Change this muam.nickhost ... (everything up to model.bin) to the path to the model.bin file (lies in cgi-bin). It is especially important if there are Russian letters on the way! And also important - all the slashes should be "/" !!!! In Windows, they are defaulted to the other side, change !!!
7. You go to the console, go to www, write - python -m http.server —cgi (2 minuses!): 8000
8. localhost: 8000 / is waiting for you :)
