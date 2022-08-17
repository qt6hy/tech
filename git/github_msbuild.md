
# Note about Github Actions with MSBuild

## References

- [Git Hub Actions入門](https://zenn.dev/hashito/articles/7c292f966c0b59)

- [GitHub ActionsでMSBuildによるビルドを行う](https://zenn.dev/shimat/articles/d9ed0345c9866e)

- [GitHub Actionsの支払いについて - GitHub Docs](https://docs.github.com/ja/billing/managing-billing-for-github-actions/about-billing-for-github-actions)

- [About GitHub-hosted runners](https://docs.github.com/ja/actions/using-github-hosted-runners/about-github-hosted-runners#supported-runners-and-hardware-resources)

- [Windows Server 2022 Datacenter - runner image](https://github.com/actions/runner-images/blob/main/images/win/Windows2022-Readme.md)

## Fix errors

### error FTK1011

```txt
FileTracker : error FTK1011: could not create the new file tracking log file:
```

This was caused by long path name. My github repo has long folder name.
To fix the problem, I made my source folder name shorten.

### error MIDL2212

```txt
midlrt : error MIDL2212: [msg]error while writing to file [context]App.winmd (HRESULT:0x80070020 - The process cannot access the file because it is being used by another process.
```

This was caused by lack of storage. My github repo is FREE public.
So, we can only use 500MB of storage.
My solution has 2 projects, one is GUI app and another is package it. To fix the problem, I changed my solution not to build `package` project.
