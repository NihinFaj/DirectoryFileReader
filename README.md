# DirectoryFileReader
Reads Excel or CSV Files from a specified directory and returns a validated json result that can be easily inserted into a datatable  


Take the following step


ReadFileFromDirectory readFileFromDirectory = new ReadFileFromDirectory();

Reads file from directory specified


var read = readFileFromDirectory.ProcessNewFiles("C//local");

Returns a result of read

{
  "ProcessedFileCount": 2,
  "UnProcessedFileCount": 1,
  "ProcessFileInformation": [
    {
      "ProcessedFileName": "LimitTemplate - Copy",
      "ProcessedFileData": "[{\"User_Name\":\"DFDGR\",\"NewFXLimit\":1000.0}]"
    },
    {
      "ProcessedFileName": "LimitTemplate2",
      "ProcessedFileData": "[{\"User_Name\":\"Kuploader\",\"NewFXLimit\":20000.0},{\"User_Name\":\"DFDG\",\"NewFXLimit\":1000.0}]"
    }
  ],
  "UnProcessFileInformation": [
    {
      "UnProcessedFileName": "LimitTemplate2 - Copy",
      "UnProccessedFileError": "No data exist for the specified file name"
    }
  ],
  "AllFileSuccessFullyRead": {
    "AllFileWasRead": true,
    "AllFileWasReadResponse": "Success"
  }
}

Where
processfilecount = total amount of processed file


UnProcessedFileCount = total amount of unprocessed file


ProcessedFileName = name of each processed file on the directory


ProcessedFileData = data of each processed file on the directory


UnProcessedFileName = name of each file on the directory


UnProccessedFileError = reason File was not processed


AllFileWasRead = validate all file was read

Note:- only xls, xlsx and csv files can be currently read
