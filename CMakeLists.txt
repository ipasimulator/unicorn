set (SOURCE_FILES
    # From `unicorn.vcxproj`
    list.c
    qemu/accel.c
    qemu/glib_compat.c
    qemu/hw/core/machine.c
    qemu/hw/core/qdev.c
    qemu/qapi/qapi-dealloc-visitor.c
    qemu/qapi/qapi-visit-core.c
    qemu/qapi/qmp-input-visitor.c
    qemu/qapi/qmp-output-visitor.c
    qemu/qapi/string-input-visitor.c
    qemu/qemu-log.c
    qemu/qemu-timer.c
    qemu/qobject/qbool.c
    qemu/qobject/qdict.c
    qemu/qobject/qerror.c
    qemu/qobject/qfloat.c
    qemu/qobject/qint.c
    qemu/qobject/qlist.c
    qemu/qobject/qstring.c
    qemu/qom/container.c
    qemu/qom/cpu.c
    qemu/qom/object.c
    qemu/qom/qom-qobject.c
    qemu/tcg-runtime.c
    qemu/util/aes.c
    qemu/util/bitmap.c
    qemu/util/bitops.c
    qemu/util/crc32c.c
    qemu/util/cutils.c
    qemu/util/error.c
    qemu/util/getauxval.c
    qemu/util/host-utils.c
    qemu/util/module.c
    qemu/util/oslib-win32.c
    qemu/util/qemu-error.c
    qemu/util/qemu-thread-win32.c
    qemu/util/qemu-timer-common.c
    qemu/vl.c
    uc.c)

add_library (unicorn SHARED ${SOURCE_FILES})
add_prep_dep (unicorn)

target_include_directories (unicorn PRIVATE
    # From `unicorn.vcxproj`
    msvc/unicorn include qemu qemu/include qemu/tcg)
