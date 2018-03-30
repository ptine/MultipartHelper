Utility class to upload file in multipart/form-data in Android

Example usage:

String charset = "UTF-8";
String requestURL = "www.example.com/upload?myId=12312";

string filePath = "/MyStorage/MySubdir/myfilename.jpg";
string fileName = filepath.substring(filepath.lastIndexOf("/")+1);

MultipartUtility multipart = new MultipartUtility(requestURL, charset);
multipart.addFormField("myFormFieldName1", "foo");
multipart.addFormField("myFormFieldName2", "bar");
multipart.addFormField("file", fileName);
multipart.addFilePart("file", new File(filePath));
String response = multipart.finish();