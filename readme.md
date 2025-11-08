# msx-example

![](./screenshot.jpg)

## install nix
determinate nix installer has flakes and nix-command enabled out of the box,
otherwise you have to enable them manually. So I recommend the easy way of
installing nix like this with everything set up:
```
curl -fsSL https://install.determinate.systems/nix | sh -s -- install --determinate --no-confirm
```

## build rom
```
nix shell nixpkgs#z88dk --command zcc +msx -create-app -subtype=rom -o main main.c
```

## run rom
```
openmsx ./main.rom
```
