# BibleInJson

The files in this repository represent the Bible in JSON format. It may be said to be an ecumenical project, as it includes translations from various Christian and Jewish traditions. As a result, it includes the Hebrew Bible (Old Testament), Apocrypha/Deuterocanon, and New Testament depending on what is included in a given translation.

The files are:

- books.json - The books of the Bible
- chapters.json - The text of the Bible, organized by chapter, with the verses for each contained in an array
- translations.json - The included translations

I created this dataset to use for a personal project I'm working on using MongoDB. I may change/add documents and fields as necessary to support my own work in the future.

All of the Biblical text was retrieved from [eBible.org](https://www.ebible.org). I downloaded the SQL scripts they provided for use with BibleWorks, modified them to work with MS SQL Server, and combined the data there. I then wrote a utilty in C# (using EF Core & Json.NET) to export them into the JSON files found here.

All of the translations selected are in the public domain per eBible.org.

Finally, a few things to note:

1. Not all translations contain all of the books listed in books.json. For example, the JPS translation does not contain the New Testament or Apocryphal books as expected.
2. Some translations number some chapters and verses differently than others, and as such they will not always align perfectly.