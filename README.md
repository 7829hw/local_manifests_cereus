# local_manifests_cereus

Local manifest for building LineageOS 24.0 for the Xiaomi Redmi 6 (cereus).
Link or copy `cereus.xml` into `.repo/local_manifests/` and run `repo sync`.

```
repo init -u https://github.com/LineageOS/android.git -b lineage-24.0 --git-lfs
mkdir -p .repo/local_manifests
curl -o .repo/local_manifests/cereus.xml \
    https://raw.githubusercontent.com/7829hw/local_manifests_cereus/lineage-24.0/cereus.xml
repo sync
source build/envsetup.sh
lunch lineage_cereus cp2a userdebug
m bacon
```
