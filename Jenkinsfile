pipeline {
  parameters {
    string(defaultValue: 'executeCall.py', description: 'PYTHON_FILE', name: 'PYTHON_FILE')
    string(defaultValue: 'checkResult.py', description: 'PYTHON_FILE2', name: 'PYTHON_FILE2')
    string(defaultValue: 'executeCall.sql', description: 'SQL_FILE', name: 'SQL_FILE')
    string(defaultValue: 'executeCall1.sql', description: 'SQL_FILE_TEMP', name: 'SQL_FILE_TEMP')
    string(defaultValue: 'C:/Users/user/PycharmProjects/pygame/plsql', description: 'FILE_PATH_PY', name: 'FILE_PATH_PY')
    string(defaultValue: 'D:/pyoracle', description: 'FILE_PATH_SQL', name: 'FILE_PATH_SQL')
    string(defaultValue: '20190701', description: 'DATA_d1', name: 'DATA_d1')
    string(defaultValue: '20190702', description: 'DATA_d2', name: 'DATA_d2')
    string(defaultValue: '20190703', description: 'DATA_d3', name: 'DATA_d3')
    string(defaultValue: '20190704', description: 'DATA_d4', name: 'DATA_d4')
    string(defaultValue: '20190705', description: 'DATA_d5', name: 'DATA_d5')
    string(defaultValue: '20190706', description: 'DATA_d6', name: 'DATA_d6')
    string(defaultValue: '20190707', description: 'DATA_d7', name: 'DATA_d7')
    string(defaultValue: '20190701', description: 'DATA_mth', name: 'DATA_mth')
  }
  agent any 
  stages {
    stage("1st schema call") {
      steps {
        //powershell 'Write-Output "Hello, World!"'
          powershell "Get-Content ${params.FILE_PATH_SQL}/${params.SQL_FILE_TEMP} | ForEach-Object {\$_ -replace ('DATA_d1','20190701') -replace ('DATA_d2','20190702') -replace ('DATA_d3','20190703') -replace ('DATA_d4','20190704') -replace ('DATA_d5','20190705') -replace ('DATA_d6','20190706') -replace ('DATA_d7','20190707') -replace ('DATA_mth','20190701')}| Set-Content ${params.FILE_PATH_SQL}/${params.SQL_FILE}"
        // execute
        //sh "python ${params.FILE_PATH_PY}/${params.PYTHON_FILE}" //本地
      }
    } 
    /*stage("2nd schema check") {
      steps {
        // execute
        sh "python ${params.FILE_PATH_PY}/${params.PYTHON_FILE2}" //本地
      }
    }*/
  }
}
