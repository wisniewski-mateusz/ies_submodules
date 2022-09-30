# How to clone a repository with a submodule in it?

To clone a directory which contains the submodule in it, you can do the following:

```
git clone git@github.com:wisniewski-mateusz/ies_submodules.git
...
cd ies_submodules
git submodule init
git submodule update
# or git submodule update --init
```

> We should check how it works when the submodule is a part of some branch only. Additionally, I don't know yet if to initialize the submodule, one has to be in the correct directory. The next way of cloning the repo with a submodule may resolve these potential problems.

or using the summarized version with the special command:

```
git clone --recurse-submodules git@github.com:wisniewski-mateusz/ies_submodules.git
```

To see more information with **status** command about the changes which were made in the submodule, the next line can be executed:

```
git config status.submodulesummary 1
```