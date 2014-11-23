##  Functional Reactive Programming

```
Observable<String> filePathObservable = downloadFileObservable()
    .map(new Func1<File, String>() {
        @Override
        public String call(File file) {
            return file.getAbsolutePath();
        }
});

// now emits file paths, not `File`s
subscription = filePathObservable.subscribe(/* Observer<String> */);
```

https://gist.github.com/staltz/868e7e9bc2a7b8c1f754
