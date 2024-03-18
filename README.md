# Finance Activity Flatpak

Finance is a simple financial planning activity. It can be integrated into classroom assignments, or else used to track finances for a school club. It might also be useful for students who wish to help their parents with home finances.

To know more refer https://github.com/sugarlabs/finance-activity

## How To Build

```
git clone https://github.com/flathub/org.sugarlabs.Finance.git
cd org.sugarlabs.Finance
flatpak -y --user install flathub org.gnome.{Platform,Sdk}//46
flatpak -y --user install org.sugarlabs.BaseApp//24.04
flatpak-builder --user --force-clean --install build org.sugarlabs.Finance.json
```

## Check For Updates

Install the flatpak external data checker
```
flatpak --user install org.flathub.flatpak-external-data-checker
```

Now to update every single module to the latest stable version use
```
cd org.sugarlabs.Finance
flatpak run --filesystem=$PWD org.flathub.flatpak-external-data-checker org.sugarlabs.Finance.json
```
