storage-proxy
=============

This repository is git flow enabled (default settings).

## Goal

The goal of this app is to show the consistent hash algorithm in use while proxing data to different storage systems.

Initialy I use folders to represent cloud storage systems. They abstract away a more complex cloud storage api, we have better network speed (drive speed) and we have unlimited number readily available.

## Request Lifecycle

### Client:

* Clients sends (html post) data to api
* Clients receives (html get) data from api

### Server:

#### receive

- api checks file size (header). should be smaller than 5 GB.
- api determines hash of filename and folders (eg. storage services) to store to
- api receives data and stores it into folder
- api should take hash of receiving data
- api should store hash and name of receiving data
- api returns hash in response

#### send

- api determines hash of filename and folders (eg. storage services) to receive from
- api streams file back from one of the folders to client

### Config:

* api needs names and hashes of folders (eg. services)

## Part of PhD-Thesis

This code is part of my PhD-Thesis: A longterm storage strategy for the cultural heritage of the Federal Republic of Germany

It is an explorative sciences project which hopefully helps me gain some new ideas on how to tacle the problem of storing digital culture for future generations. I'm not responsible for forks or what YOU do with the code.

## License

Free Science for a better tomorow

Copyright (c) 2012 Samuel Goebert

Permission is hereby granted, free of charge, to any person obtaining a copy of this software and associated documentation files (the "Software"), to deal in the Software without restriction, including without limitation the rights to use, copy, modify, merge, publish, distribute, sublicense, and/or sell copies of the Software, and to permit persons to whom the Software is furnished to do so, subject to the following conditions:

The above copyright notice and this permission notice shall be included in all copies or substantial portions of the Software.

THE SOFTWARE IS PROVIDED "AS IS", WITHOUT WARRANTY OF ANY KIND, EXPRESS OR IMPLIED, INCLUDING BUT NOT LIMITED TO THE WARRANTIES OF MERCHANTABILITY, FITNESS FOR A PARTICULAR PURPOSE AND NONINFRINGEMENT. IN NO EVENT SHALL THE AUTHORS OR COPYRIGHT HOLDERS BE LIABLE FOR ANY CLAIM, DAMAGES OR OTHER LIABILITY, WHETHER IN AN ACTION OF CONTRACT, TORT OR OTHERWISE, ARISING FROM, OUT OF OR IN CONNECTION WITH THE SOFTWARE OR THE USE OR OTHER DEALINGS IN THE SOFTWARE.