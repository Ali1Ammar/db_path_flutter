# dbpath

get database path getDataBasePath()

## Getting Started

this package has only one function getDataBasePath() to get database path for android 
as path_provider doesnt have it 
for ios there is not database path you should use getApplicationDocumentsDirectory from path_provider 

somethinge like this 

dart'''
Future<String> getDBPath() async => isAndroid
    ? (await getDataBasePath())!
    : (await getApplicationDocumentsDirectory()).path;

'''