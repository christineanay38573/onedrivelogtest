christine.anay38573@outlook.com
except git: SDYrdshytsERTeqwHDFBsd
git: christine38573
have postman account

- To get access token, you should register App using this url : https://portal.azure.com/#view/Microsoft_AAD_RegisteredApps/ApplicationsListBlade

- After register App, follow instructions from url below.

  consult this : https://docs.microsoft.com/en-us/onedrive/developer/rest-api/getting-started/msa-oauth?view=odsp-graph-online

  ex : https://login.live.com/oauth20_authorize.srf?client_id=4be8d586-03e5-4766-9d12-1eda0e9a6aef&scope=Files.ReadWrite.All&response_type=token&redirect_uri=https://google.com
  
  response ex : https://www.google.com/#access_token=EwBwA8l6BAAUkj1NuJYtTVha%2bMogk%2bHEiPbQo04AAVQnRsyXJp/giZYJVYb4AN59P0ida26NTxuV1dd09YHjf%2b/JvPgZw/muBwIoE94N%2bwfyd/gKWudiq/%2bQGzZoa9Z6fv230f0/djZ8fqipBHKmysBKrpD83ob9uO4tLh%2bSkq40MgibI3LdnrzV6tactFw7d4BfrlNn/JajpTweeuo0STJbHbOuI6cL16XeDa3qR5JsruFrUFPtqSNwamf3phd%2bwigdDOeAFxUQIpNRVghWdRxiYvMzXMKcrfLl3RMjfjrY1Tzu9NFl7wlBlCK6NgycFtZjwE3eTKDzPXYPyq1fYjxz3ZD1djPGusMuUsv5i1EpIKYj6EICMuK3IBcGGQ8DZgAACPBwC9P5jlVKQAIW%2beKjyiYkf8o8sn5PmSWn%2by%2boS60oWPevtgwB0oI0t/VrsKmpCKWprDHf2ojOJWS3h5KVG2elmRfWsbssG%2bBt7UVHbo9vAEBkZ2WD7Y1lfjvjGtgsFhK5LMLVVGm10oNwK2es9TZMq7Vj/nBpwb86%2bftdZ2/IX83PqQddp17bXdAW3mPlDWH9VH/RMEUF7Kpb4Ir5J2SJlS1H7SmZaEqe4QiOdwmgQHF9rZXucON2zlUyPsJp1%2bfd9h9xQ4zduocx8rMuyjJEP/9nBtde0Om%2bfFxcRWDRwlNDxCxrJ%2biwfhCf9RxuS1lt5JLPBDbmJKA9mrNl58YSOwPN9M%2bRIfUWPyM48o9cWQWZvdPeBM/gF8QncTrjYyZQcW6CSOjfVrfRsJfCib94eonudWQlL%2byLdpL6Wqt5o3CNIq9/h51DJUSCzHjdFdbGpIXNanQgrEEDpI5pRQtynVp2QzMfcFye1yz59kpWarQ%2b7oOkHZ7lEwktAqMRC18KqbzjND5J3httjkRNUZHTBneKX0%2bS3hmzWi9qJVZHnG5uqNADitFKyc/wMFr8JoHTe5lDDAOQJ%2bA07yZ/O8HRW9ul%2bAoLXXoiRno9Xf51w6P/12x11RWh%2biYBI1eRm29xY6T3YONAdHVwE158vXcoyMyt%2b8wwMHCQZ2L1vfvQJ0MoqIH7q7OZ0jKqYutLt8ZeD3VbkGOFGu1DI47WWKgkPbKINUU1zL/x6zUwNljAWX3WCGIXIA1%2boUcSiZfPO1WdbFq5rb0TiK6PAg%3d%3d&token_type=bearer&expires_in=3600&scope=Files.ReadWrite.All%20Files.Read&user_id=AAAAAAAAAAAAAAAAAAAAAG6iIuWOs8qaP5dPSIiqlkk

- Onedrive Rest API

  list root items : GET https://graph.microsoft.com/v1.0/me/drive/root/children?select=@microsoft.graph.downloadUrl,createdDateTime,id,name,size&orderby=createdDateTime desc
  
  list items : GET https://graph.microsoft.com/v1.0/me/drive/items/72E91F67C4BC3F45!107/children?select=@microsoft.graph.downloadUrl,createdDateTime,id,name,size&orderby=createdDateTime desc&top=1
  
    Response : 
    {
        "@odata.context": "https://graph.microsoft.com/v1.0/$metadata#users('christine.anay38573%40outlook.com')/drive/items('72E91F67C4BC3F45%21107')/children",
        "@odata.count": 3,
        "@odata.nextLink": "https://graph.microsoft.com/v1.0/me/drive/items/72E91F67C4BC3F45!107/children?select=%40microsoft.graph.downloadUrl%2ccreatedDateTime%2cid%2cname%2csize&orderby=createdDateTime+desc&top=1&$skiptoken=Mg",
        "value": [
            {
                "@microsoft.graph.downloadUrl": "https://public.am.files.1drv.com/y4mDTmU2bUpAHtHr8-2EYSqqGzaH0Qvd5nVAkxx2fh8DCvGqdTaQYbziw4BTiHkN8zYLZl-O2q6vLFx5xHS8eJ4JUhCgqVDNvrqrUxaacMOB3PcrES_CgY3HZMirnevjLS_e8mB7CXzFKa-mDNCCmLDmNhUFPwflGwylIZBtxZKd9YWE4OU1ZiOtQvIk7rVUSBLpM7FhNDfMDLRFGbu9MMpZErGWYETimzlC2xDDMl8GYgCB-IMsvFGiDuZrSGOK6gZ",
                "createdDateTime": "2022-07-05T06:53:29.213Z",
                "id": "72E91F67C4BC3F45!110",
                "name": "sdtrhjgf202207051148.txt",
                "size": 19
            }
        ]
    }
  
  upload files : PUT https://graph.microsoft.com/v1.0/me/drive/items/72E91F67C4BC3F45!107:/sdtrhjgf202207051148.txt:/content
  
    Response : 
    {
      "@odata.context": "https://graph.microsoft.com/v1.0/$metadata#users('christine.anay38573%40outlook.com')/drive/items/$entity",
      "@microsoft.graph.downloadUrl": "https://cwazrq.am.files.1drv.com/y4p-QiPwaqA01cTk7G8hq466DMevGwB3xfJdi9E3uMJbI5LEwPuXA7EqjIS2Z99VKdrNJzuo5a1D2WwsiHrN924tPvC7MfVpPoZJI7RP8JGgviUPmgN1tPgtRCPTtqOeu6HFsgLD8Qlk_l4NFo9CW4Cmi4bD98w4sx1ZFP6XUl7WELd4Yz2RgNm6_Ts998yogTb0uXRJsZWUuGLWSm7YUXVRsTe5LKPT4lvEQGGeTkMnjr_8twkEQF29IxCM0AJ3pSv",
      "createdDateTime": "2022-07-05T06:53:29.213Z",
      "cTag": "aYzo3MkU5MUY2N0M0QkMzRjQ1ITExMC4yNTc",
      "eTag": "aNzJFOTFGNjdDNEJDM0Y0NSExMTAuMA",
      "id": "72E91F67C4BC3F45!110",
      "lastModifiedDateTime": "2022-07-05T06:53:29.213Z",
      "name": "sdtrhjgf202207051148.txt",
      "size": 19,
      "webUrl": "https://1drv.ms/t/s!AEU_vMRnH-lybg",
      "reactions": {
          "commentCount": 0
      },
      "createdBy": {
          "application": {
              "displayName": "abcd",
              "id": "40c0995f"
          },
          "user": {
              "displayName": "Christine Anay",
              "id": "72e91f67c4bc3f45"
          }
      },
      "lastModifiedBy": {
          "application": {
              "displayName": "abcd",
              "id": "40c0995f"
          },
          "user": {
              "displayName": "Christine Anay",
              "id": "72e91f67c4bc3f45"
          }
      },
      "parentReference": {
          "driveId": "72e91f67c4bc3f45",
          "driveType": "personal",
          "id": "72E91F67C4BC3F45!107",
          "name": "testlog",
          "path": "/drive/root:/testlog"
      },
      "file": {
          "mimeType": "text/plain",
          "hashes": {
              "quickXorHash": "9E4mguUdgjTMAQR1kwMb3hAGMoA=",
              "sha1Hash": "EE2BB74154BDF2F87A1F18DE9F3FE3BD6E63C6C1",
              "sha256Hash": "552EC1569907A781531F2EF86F06CE20029FB0B56B61C19C421868A035B802DA"
          }
      },
      "fileSystemInfo": {
          "createdDateTime": "2022-07-05T06:53:29.213Z",
          "lastModifiedDateTime": "2022-07-05T06:53:29.213Z"
      }
  }
  
  consult this : https://docs.microsoft.com/en-us/onedrive/developer/rest-api/api/driveitem_list_children?view=odsp-graph-online
  consult this : https://docs.microsoft.com/en-us/onedrive/developer/rest-api/api/driveitem_put_content
