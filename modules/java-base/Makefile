include common.gmk

ifeq ($(arch),aarch64)
java-targets :=
else
java-targets := obj/jni/monitor.so obj/jvm/jni_helpers.o obj/jvm/java_api.o obj/balloon/jvm_balloon.o
endif

module: all

all: $(init) $(java-targets)

init:
	@echo "  MKDIRS"
	$(call very-quiet, mkdir -p obj/jni)
	$(call very-quiet, mkdir -p obj/jvm)
	$(call very-quiet, mkdir -p obj/balloon)
.PHONY: init

clean:
	$(call very-quiet, $(RM) -rf obj)
