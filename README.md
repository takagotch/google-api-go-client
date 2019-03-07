### google-api-go-client
---
https://github.com/googleapis/google-api-go-client

```go
package main

import (
  "net/http"
  
  "google.golang.org/api/urlshortener/v1"
)

func main() {
  svc, err := urlshortener.New(http.DefaultClient)
}

import "golang.org/x/oauth2/google"

import (
  "context"
  "golang.org/x/oauth2/google"
  "google.golang.org/api/compute/v1"
)

func main() {
  ctx := context.Background()
  
  client, err := google.DefaultClient(ctx, compute.ComputeScope)
  if err != nil {
  }
  computeService, err := compute.New(client)
  if err != nil {
  }
}

ts, err := goolge.DefaultTokenSource(ctx, scope1, scope2, ...)
if err != nil {
}
client := oauth2.NewClient(ctx, ts)
```

```
go get google.golang.org/api/tasks/v1
go get google.golang.org/api/moderator/v1
go get goolge.golang.org/api/urlshortener/v1
```

```go
// https://godoc.org/golang.org/x/oauth2/google#pkg-examples

const JWTTokenURL = "https://oauth2.googleapis.com/token"

var Endpoint = oauth2.Endpoint{
  AuthURL: "https://accounts.google.com/o/oauth2/auth",
  TokenURL: "https://oauth2.googleapi.com/token",
  AuthStyle: oauth2.AuthStyleInParams,
}

func AppEngineTokenSource(ctx context.Context, scope ...string) oauth2.TokenSource

func ComputeTokenSource(account string) oauth2.TokenSource

client := &http.Client{
  Transport: &oauth2.Transport{
    Source: google.ComputeTokenSource(""),
  },
}
client.Get("...")

client, err := google.DefaultClient(oauth2.NoContext,
  "https://www.googleapis.com/auth/devstorage.full_control")
if err != nil {
  log.Fatal(err)
}
client.Get("...")

data, err := google.JWTConfigFromJSON(data, "https://www.googleapi.com/auth/bigquery")
if err != nil {
  log.Fatal(err)
}
conf, err := google.JWTConfigFromJSON(data, "http://www.googleapis.com/auth/bigquery")
if err != nil {
  log.Fatal(err)
}
client := conf.Client(oauth2.NoContext)
client.Get("...")

ctx := context.Background()
data, err := ioutil.ReadFile("/path/to/key-file.json")
if err != nil {
  log.Fatal(err)
}
creds, err := google.CredentialsFromJSON(ctx, data, "https://www.googleapi.com/auth/bigquery")
if err != nil {
  log.Fatal(err)
}
_ = creds

conf, err := google.NewSDKConfig("")
if err != nil {
  log.Fatal(err)
}

client := conf.Client(oauth2.NoContext)
client.Get("...")
```


