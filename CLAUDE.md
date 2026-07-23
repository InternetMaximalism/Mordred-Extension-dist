# Repository instructions

## Git commit identity

Every commit in this repository must use `mordred-poc <poc@localhost>` as both
the author and committer identity. Do not rely on or modify the user's local or
global Git configuration. Create commits with:

```sh
git -c user.name=mordred-poc -c user.email=poc@localhost commit ...
```
