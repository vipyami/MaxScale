add_executable(test_mysql_users test_mysql_users.c)
add_executable(test_hash testhash.c)
add_executable(test_hint testhint.c)
add_executable(test_spinlock testspinlock.c)
add_executable(test_filter testfilter.c)
add_executable(test_buffer testbuffer.c)
add_executable(test_dcb testdcb.c)
add_executable(test_modutil testmodutil.c)
add_executable(test_poll testpoll.c)
add_executable(test_service testservice.c)
add_executable(test_server testserver.c)
add_executable(test_users testusers.c)
add_executable(test_adminusers testadminusers.c)
add_executable(testmemlog testmemlog.c)
target_link_libraries(test_mysql_users MySQLClient fullcore)
target_link_libraries(test_hash fullcore)
target_link_libraries(test_hint fullcore)
target_link_libraries(test_spinlock fullcore)
target_link_libraries(test_filter fullcore)
target_link_libraries(test_buffer fullcore)
target_link_libraries(test_dcb fullcore)
target_link_libraries(test_modutil fullcore)
target_link_libraries(test_poll fullcore)
target_link_libraries(test_service fullcore)
target_link_libraries(test_server fullcore)
target_link_libraries(test_users fullcore)
target_link_libraries(test_adminusers fullcore)
target_link_libraries(testmemlog fullcore)
add_test(testMySQLUsers test_mysql_users)
add_test(TestHash test_hash)
add_test(TestHint test_hint)
add_test(TestSpinlock test_spinlock)
add_test(TestFilter test_filter)
add_test(TestBuffer test_buffer)
add_test(TestDCB test_dcb)
add_test(TestModutil test_modutil)
add_test(TestPoll test_poll)
add_test(TestService test_service)
add_test(TestServer test_server)
add_test(TestUsers test_users)
add_test(TestAdminUsers test_adminusers)
add_test(TestMemlog testmemlog)
set_tests_properties(testMySQLUsers
  TestHash
  TestHint
  TestSpinlock
  TestFilter
  TestBuffer
  TestDCB
  TestModutil
  TestPoll
  TestService
  TestServer
  TestUsers
  TestAdminUsers
  TestMemlog PROPERTIES ENVIRONMENT MAXSCALE_HOME=${CMAKE_BINARY_DIR}/)
