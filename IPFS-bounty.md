## IPFS : IPFS-Filecoin based Web3 storage has been used for permanent decentralized storage of DAO documents on DAO drive


##### https://github.com/Disha1998/TheDAO-Tool/blob/master/src/utils/Web3Storage.js
##### https://github.com/Disha1998/TheDAO-Tool/blob/master/src/pages/Drive.js
```
import { Web3Storage } from "web3.storage";
function getAccessToken() {
  // If you're just testing, you can paste in a token
  // and uncomment the following line:
  // return 'paste-your-token-here'
  // In a real app, it's better to read an access token from an
  // environement variable or other configuration that's kept outside of
  // your code base. For this to work, you need to set the
  // WEB3STORAGE_TOKEN environment variable before you run your code.
  return process.env.REACT_APP_WEB3_STORAGE_API_KEY;
}

function makeStorageClient() {
  return new Web3Storage({ token: getAccessToken() });
}
export default async function   storage(files) {
  const client = makeStorageClient();
  const cid = await client.put(files);
  return cid;
}
 let cid = await storage(data);
```

<img width="1435" alt="MicrosoftTeams-image (7) (1)" src="https://user-images.githubusercontent.com/69969675/162677793-4ad78f1e-cd1c-4d03-9fdd-af9147edc1fc.png">


