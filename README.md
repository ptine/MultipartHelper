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
MultipartUtility multipart = new MultipartUtility(requestURL, charset);<br>
multipart.addFormField("myFormFieldName1", "foo");<br>
multipart.addFormField("myFormFieldName2", "bar");<br>
multipart.addFormField("file", fileName);<br>
multipart.addFilePart("file", new File(filePath));<br>
String response = multipart.finish();<br>