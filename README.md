# jsonfs

This is an informal proposal for a file system in a single file of the JSON format.

Each item that is an object is a **directory**.

```javascript
{
  "this-is-a-blank-directory": {
  }
}
```

The root object of a JSON file is the root directory of that file's respective jsonfs.

Each item inside a directory that is *not* an object (that is, a number, a string, an array or a special value) is a **file**. Objects in arrays aren't parsed as directories, so you can keep a jsonfs file in a jsonfs file. :P

```javascript
{
  "this-is-a-file": true,
  "this-is-a-directory-with-some-files": {
    "a-number": 123,
    "a-string": "A string",
    "a-boolean": true,
    "an-array": [
      {
        "this-object-isnt-a-directory": true
      }
    ]
  }
}
```

The file name of each item is that item's name.

That's about all.

<a rel="license" href="http://creativecommons.org/licenses/by/4.0/"><img alt="Creative Commons License" style="border-width:0" src="https://i.creativecommons.org/l/by/4.0/88x31.png" /></a><br />This work is licensed under a <a rel="license" href="http://creativecommons.org/licenses/by/4.0/">Creative Commons Attribution 4.0 International License</a>.

## Renderers

The four kinds of lists in the [MdProp](https://github.com/schas002/mdprop) informal proposal seem to somehow apply to jsonfs. For example, renderers inform the user of something about the file system in the file.

*No renderers yet. When you made one, share with us!*

## Validators

Validators do some checks on the file system in the file, or the file itself.

*No validators yet. When you made one, share with us!*

## Parsers

If you have a module in your lang for JSON, then it is your local parser. You can, however, make specialised parsers for jsonfs files.

*No parsers yet. When you made one, share with us!*

## Converters

Converters convert files in the jsonfs between types, file systems (copy the file into a file on the physical file system), et cetera.

*No converters yet. When you made one, share with us!*
