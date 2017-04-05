<img src="https://avatars2.githubusercontent.com/u/2810941?v=3&s=96" alt="Google Cloud Platform logo" title="Google Cloud Platform" align="right" height="96" width="96"/>

# Google Cloud Speech API Node.js Samples

The [Cloud Speech API][speech_docs] enables easy integration of Google speech
recognition technologies into developer applications.

[speech_docs]: https://cloud.google.com/speech/

## Table of Contents

* [Setup](#setup)
* [Samples](#samples)
  * [Recognize](#recognize)

## Setup

1. Read [Prerequisites][prereq] and [How to run a sample][run] first.
1. Install dependencies:

        npm install

[prereq]: ../README.md#prerequisities
[run]: ../README.md#how-to-run-a-sample

## Samples

### Recognize

View the [documentation][recognize_docs] or the [source code][recognize_code].

__Usage:__ `node recognize.js --help`

```
Commands:
  sync <filename>     Detects speech in a local audio file.
  sync-gcs <gcsUri>   Detects speech in an audio file located in a Google Cloud Storage bucket.
  async <filename>    Creates a job to detect speech in a local audio file, and waits for the job to complete.
  async-gcs <gcsUri>  Creates a job to detect speech in an audio file located in a Google Cloud Storage bucket, and
                      waits for the job to complete.
  stream <filename>   Detects speech in a local audio file by streaming it to the Speech API.
  listen              Detects speech in a microphone input stream.

Options:
  --help            Show help                                                                                  [boolean]
  --encoding, -e                                                                          [string] [default: "LINEAR16"]
  --sampleRate, -r                                                                             [number] [default: 16000]

Examples:
  node recognize.js sync ./resources/audio.raw -e LINEAR16 -r 16000
  node recognize.js async-gcs gs://my-bucket/audio.raw -e LINEAR16 -r 16000
  node recognize.js stream ./resources/audio.raw  -e LINEAR16 -r 16000
  node recognize.js listen

For more information, see https://cloud.google.com/speech/docs
```

[recognize_docs]: https://cloud.google.com/speech/docs
[recognize_code]: recognize.js
