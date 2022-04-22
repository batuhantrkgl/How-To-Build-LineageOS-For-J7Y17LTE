# How-To-Build-LineageOS-For-J7Y17LTE
What Do You Need?
-A Computer With Specs: Mininum 16GB Ram And 150+ GB Stroage And Ubuntu 20.04 Or 18.04
-A Working Brain.
-Tester For Your Device
-Mininum 100GB Internet
## SYNC The LineageOS!
Now First Create Dir For Your Rom. like this: 
```mkdir los17```
Now Second İnit The LineageOS Repo
Like This:
```repo init -u https://github.com/LineageOS/android -b lineage-17.1```
Here! Your Branch Is `LineageOS 17.1` But How To Change It? 
-b `your-branch` in here -b feature says: `I Want The Your Custom Rom BRANCH!!!`
## Sync The Rom...
What? I Already İnitted Repo Whats This? so you need the sync the rom the working on it.. 
just paste the this command 
```repo sync -c -j$(nproc --all) --force-sync --no-clone-bundle --no-tags```
And Wait A 10 Minute-2 Hours... Thats Very Long ;(
## Working On The Rom
You Need The Sync Your Device Tress To Build İt. 
now paste this commands:
```git clone https://github.com/samsungexynos7870/android_device_samsung_j7y17lte -b crdroid device/samsung/j7y17lte
git clone https://github.com/samsungexynos7870/android_device_samsung_universal7870-common -b lineage-17 device/samsung/universal7870-common
git clone https://github.com/samsungexynos7870/android_kernel_samsung_exynos7870 -b aosp kernel/samsung/exynos7870
git clone https://github.com/samsungexynos7870/android_vendor_samsung_j7y17lte -b common vendor/samsung/j7y17lte
git clone https://github.com/samsungexynos7870/android_vendor_samsung_universal7870-common -b common vendor/samsung/universal7870-common
git clone https://github.com/samsungexynos7870/android_hardware_samsung -b lineage-17.1 hardware/samsung
```
now all device tress synced!
## Build The Rom 
You Need The Setup The Evrioment But How? 
use this command: 
```. build/envsetup.sh```
and now it ready for build. first use the `lunch` command and select the `lineage_j7y17lte-userdebug` now make the build. use: 
```make bacon```
and now the build started! Good Luck!












## Thanks For MAXX, Exynos7870 And LineageOS
