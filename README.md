package main

import (
         "net/http"
	 "io"
)

func main() {
	http.HandleFunc("/", index)
	http.ListenAndServer(":80", nil)
}

func index(w http.ResponseWriter, r *http.Request){
        io.WritesString(w, "hello World")
}
