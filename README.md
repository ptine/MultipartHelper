<h2>Utility class to upload file in multipart/form-data in Android</h2>

Example usage:<br>
<br>
<br>
String charset = "UTF-8";<br>
<br>
String requestURL = "www.example.com/upload?myId=12312";<br>
<br>
string filePath = "/MyStorage/MySubdir/myfilename.jpg";<br>
string fileName = filepath.substring(filepath.lastIndexOf("/")+1);<br>
<br>
MultipartHelper  multipart = new MultipartHelper (requestURL, charset);<br>
multipart.setFormField("myFormFieldName1", "foo");<br>
multipart.setFormField("myFormFieldName2", "bar");<br>
multipart.setFormField("file", fileName);<br>
multipart.setFilePart("file", new File(filePath));<br>
String response = multipart.finish();<br>