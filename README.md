# treepath

Treepath takes an array of pathnames and gives you back an object representation of that path hierarchy.


## Usage

#### The paths we want to transform into an Object structure

```javascript
var paths = [
  'Users/Joe/Pictures/image-1.jpg',
  'Users/Joe/Documents/resume.2014.pdf',
  'Users/Joe/Music/favorite-track.mp3',

  'Users/Joe/temp.txt',
  'Users/Joe/log.txt',
  
  'Users/Joe/Desktop/screenshot_v1.2.jpg',
  'Users/Joe/Desktop/screenshot_v1.1.jpg',
  
  '/random-file-9.md',
  'other.doc'
];
```

#### Calling it

```javascript
var tree = treepath(paths);
```

**Output:**

```javascript
{
  "root": {
    "path": "",
    "files": [
      "random-file-9.md",
      "other.doc"
    ]
  },
  "Users": {
    "path": "Users/",
    "files": []
  },
  "Joe": {
    "path": "Users/Joe/",
    "files": [
      "temp.txt",
      "log.txt"
    ]
  },
  "Pictures": {
    "path": "Users/Joe/Pictures/",
    "files": [
      "image-1.jpg"
    ]
  },
  "Documents": {
    "path": "Users/Joe/Documents/",
    "files": [
      "resume.2014.pdf"
    ]
  },
  "Music": {
    "path": "Users/Joe/Music/",
    "files": [
      "favorite-track.mp3"
    ]
  },
  "Desktop": {
    "path": "Users/Joe/Desktop/",
    "files": [
      "screenshot_v1.2.jpg",
      "screenshot_v1.1.jpg"
    ]
  }
}
```
