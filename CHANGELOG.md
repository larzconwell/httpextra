### Oct 12, 2013
- Don't use global variable to handle content types, most functions and methods taking a request
  now need a content type map, with MIME type as the key

### Oct 05, 2013
- Don't filter out "token" params in logs, since token param authentication isn't supported anymore

### Sep 24, 2013
- Add ParseForm which sends a 400 on form parse errors

### Sep 23, 2013
- Response is now a struct holding response writer and request, with Send and SendDefault methods
  which take any body to send instead of map.

### Sep 22, 2013
- Add Marshal field to ContentType
- Add DefaultContentType to get default content type, and replace ContentTypeSupported with
  RequestContentType which returns a content type
- SlashHandler only replaces slash if url is not "/"
- Add Response map and routine to send status with body
- Accept header with "\*/\*" gets first supported content type

### Sep 21, 2013
- Add ResponseLogger
- Add NotFoundHandler, LogHandler, SlashHandler, and ContentTypeHandler handlers
- Add ContentType and routines to get a request content type
