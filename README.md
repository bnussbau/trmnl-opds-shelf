## 📚 OPDS Bookshelf for TRMNL

Display your personal bookshelf by connecting to an OPDS feed. 

Remember when people kept bookshelves in their living rooms? Guests would browse the spines, spot a favorite title and suddenly you were deep in a great conversation. But now, in the age of e-readers and digital libraries, our books are invisible. No one knows what you’re reading. The bookshelf has disappeared.

**OPDS Bookshelf for TRMNL brings it back.**

Display your personal digital shelf, live from any OPDS-compatible server, directly onto your TRMNL device. It's the perfect companion for TRMNL Guest Mode, turning your living room e-ink screen into a silent conversationalist. Visitors can browse your current reads and maybe even borrow a recommendation.

![image]()

OPDS (Open Publication Distribution System) is an open standard designed to simplify and decentralize the distribution of digital publications. OPDS catalogs let users easily browse, search, and download content across compatible apps and devices.

## ✨ Features
* Connects to any OPDS-compatible server (like Calibre-Web, Calibre (Content Server), Komga, or Strump)
* Displays shelf on your TRMNL screen
* 3 Layouts: 
  * Cover only Grid
  * Cover + Author & Title Grid
  *  List View (Author + Title)
*  Configurable for TRMNL "Guest Mode" (double-click the button on the back of your device, if configured as special function)

### Compatibility

#### Server
* Calibre
* Calibre Web
* Komga
* Strump 
* ..

#### Reader
* KOReader (Kindle, Kobo, PocketBook, Android and desktop Linux)
* ...

List of compatible OPDS Servers and Reader Applications: [awesome-opds](https://github.com/opds-community/awesome-opds?tab=readme-ov-file)

More Information on OPDS: [opds.io](https://opds.io/)

## Example

### Use with Calibre Web

1. Set up Calibre Web (https://github.com/janeczku/calibre-web)
2. Create a Shelf and add the books you want to show (select "Share with everyone")
3. To expose the feed without Authentication enable "Anonymous browsing" (Admin > Edit Basic Configuration > Feature Configuration > Enable Anonymous Browsing)
4. Get your feed and set it as polling URL in the TRMNL recipe. Copy the shelf URL and prefix /shelf with /opds/shelf (e.g. https://calibre-web.example/opds/shelf/1). Note: without anonymous browsing enabled, you'll need to provide Basic Auth credentials, eg. https://User:Passw0rd@calibre-web.example/opds/shelf/1

### Development
Can be served via [trmnlp](https://github.com/usetrmnl/trmnlp). Install trmnlp and run
```
trmnlp serve
```