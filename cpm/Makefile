# Path to Linux utilities
ZXCC = zxcc

# Path to CP/M utilities
ZSM4 = ../../Tools/cpm/zsm4.com
TKB  = ../../Tools/cpm/tkb.com

.SUFFIXES:
.SUFFIXES: .mac .rel

SRCS = cpm.mac

OBJS = $(SRCS:.mac=.rel)
XRFS = $(SRCS:.mac=.crf)

all: cpm.tsk

# *.inc and .lib files are copied from the latest RSX280 build
# in the libs/fcslib and libs/syslib sub-directories
$(OBJS): %.rel: %.mac *.inc
	$(ZXCC) $(ZSM4) -"=$</l"

cpm.tsk: $(OBJS) syslib.lib fcslib.lib
	$(ZXCC) $(TKB) -"$@,cpm,cpm=cpm,fcslib/lb,syslib/lb/task=...CPM/asg=TI:5,SY:1-4"

clean:
	rm -f *.com *.rel *.prn *.sym *.map core *.tsk *~ *.\$$\$$\$$
