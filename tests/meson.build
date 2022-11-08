configure_file(input : 'unit-test.h.in',
               output : 'unit-test.h',
               configuration : cdata)

incdir = include_directories('../src')

bandwidth_server_one = executable(
    'bandwidth-server-one', 'bandwidth-server-one.c',
    link_with : modbuslib,
    include_directories : incdir
)

bandwidth_server_many_up = executable(
    'bandwidth-server-many-up', 'bandwidth-server-many-up.c',
    link_with : modbuslib,
    include_directories : incdir
)

bandwidth_client = executable(
    'bandwidth-client', 'bandwidth-client.c',
    link_with : modbuslib,
    include_directories : incdir
)

random_test_server = executable(
    'random-test-server', 'random-test-server.c',
    link_with : modbuslib,
    include_directories : incdir
)

random_test_client = executable(
    'random-test-client', 'random-test-client.c',
    link_with : modbuslib,
    include_directories : incdir
)

unit_test_server = executable(
    'unit-test-server', 'unit-test-server.c',
    link_with : modbuslib,
    include_directories : incdir
)

unit_test_client = executable(
    'unit-test-client', 'unit-test-client.c',
    link_with : modbuslib,
    include_directories : incdir
)

test('unit-tests', find_program('unit-tests.sh'),
     workdir : meson.current_build_dir())
