[[201/README|Module 201]]
# Class 13 Reading Assignment

Reading assignment 'Read 13'

## Questions and Answers

### Local Storage & How To Use It On Websites

1. Why would a developer use local storage for a web application? It allows the user to save information that the user can use to make using the website easier and smoother.
2. What information should not be stored in local storage? Important or private information that can be retrieved by unwanted users.
3. Local storage can store what type of data? How would you convert it to that type before storing? It can story a string, and you will need to use the `JSON.stringify()` and `JSON.parse()` methods to accurately store it within local storage.

## Notes

Here are the notes I’ve taken while reading the following blogs:

[Local Storage & How To Use It On Websites](https://www.smashingmagazine.com/2010/10/local-storage-and-how-to-use-it/)

## Understanding Local Storage

> A cookie is a text file hosted on the user’s computer and connected to the domain that your website runs on. You can store information in them, read them out and delete them.

Cookies can only store up to 4 KB of data, and can have security/privacy issues.

HTML5 supports local storage and you can use JavaScript by using the `localStorage` or `sessionStorage` methods.

Even though HTML and JS `localStorage` is better, there are still ways that it potential hackers can retrieve a users private information.

Local storage can only store strings, but to work around this you can use `JSON.stringify()` and `JSON.parse()` this will ensure the data is collected within the localStorage Object appropriately.
