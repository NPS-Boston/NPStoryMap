# NPStoryMap
Builder webpage that generates a story map like widget from a CSV config
file.
Essentially, the widget enables authors to tell a story that follows a geographic path. Every "stop" has a geographic view and/or marker with a popup. Below the map is a slideshow that follows each view that can showcase any html content related to each view. For some examples, check out:
* [https://www.nps.gov/articles/helen-lee-franklin.htm](https://www.nps.gov/articles/helen-lee-franklin.htm)
* [https://www.nps.gov/articles/-god-made-me-a-man-not-a-slave-the-arrest-of-anthony-burns.htm](https://www.nps.gov/articles/-god-made-me-a-man-not-a-slave-the-arrest-of-anthony-burns.htm)

## Installation
Builder is a simple webpage with several dependencies. Just use npm to
install dependencies and run on a http server. Dependencies are jQuery,
PapaParse, Mustache.js, and Bootstrap (which also has its own dependency of
popper.js)
Two dependencies use a CDN rather than local library hosting as they are the
dependencies: Slick.js and NPMap. These dependencies are loaded by the code
snippet when pasted into a production webpage. If these libraries are broken
in the builder, they will be broken in the client.

## Usage
Open index.html in a browser and follow on-screen instructions to build a
code snippet. The primary pieces required are a CSV snippet of data and two
templates with Mustache templating.
### Required fields in CSV
CSV needs to have, at a minimum, the following table headers:
1. 'latitude' - decimal number of a point's latitude
2. 'longitude' - decimal number of a point's longitude
3. 'zoom' - integer of zoom level for a point's view (0-19, 19 is lowest level)                                                                                                                                    
4. 'marker' - a number, letter, or string from the [Maki icon set](https://labs.mapbox.com/maki-icons/) i.e. 'circle' or 'pitch', etc.

Ideally you would also have fields for marker popup text and slide content, such as an image URL, alt text for the image, etc.
