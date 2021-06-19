# NeoHomeBrew's Monitor Test Tool in NeoSD format

I don't own this software, NeoHomeBrew is the author. This repo is merely his [test suite rom](http://www.neohomebrew.com/neo-geo-monitor-test.php) in NeoSD format.

## how to create

1. download NeoHomeBrew's test rom and unrar it
2. add the missing v, s and m roms with dummy files
  * `dd if=/dev/zero of=monitor-test-s1.bin bs=128k count=1`
  * `dd if=/dev/zero of=monitor-test-m1.bin bs=128k count=1`
  * `dd if=/dev/zero of=monitor-test-v1.bin bs=2M count=1`
  * `dd if=/dev/zero of=monitor-test-v2.bin bs=2M count=1`
3. create the .neo file with [neosdconv](https://github.com/city41/neosdconv)
  * `neosdconv -i . -o testsuite.neo -n 'Test Suite 240' -g Other -y 2021 -m NeoHomeBrew`



