# poznatky které v budoucnu dodělat na notebooku X1 nano

[ ] - startovat kernel s parametrem "i915.enable_psr=0", lze vyřešit pomocí příkazu "sudo kernelstub -a "i915.enable_psr=0"" - toto by mělo vyřešit trhání obrazovky na notebooku lenovo thinkpad x1 nano s intel grafickou kartou
[ ] - nastav zvuk na 4.0 oproti původním 2.0

Níže uvedený kód vyřeší trhání oprazu: Uložit do /etc/X11/xorg.conf.d/99-intel.conf 

Section "Device"
  Identifier "Intel Graphics"
  Driver "intel"
  Option "TripleBuffer" "true"
  Option "TearFree" "true"
EndSection
