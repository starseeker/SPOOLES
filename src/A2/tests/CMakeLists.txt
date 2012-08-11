include_directories(
  ${CMAKE_CURRENT_SOURCE_DIR}/../../../include
  )

#
#  ************ norms tests *************
#
add_executable(tester_spooles_norms test_norms.c)
target_link_libraries(tester_spooles_norms spooles ${M_LIBRARY})
set(msglvl   2)
set(msgFile  stdout)
set(type     2)
set(nrow     10)
set(ncol     20)
set(inc1     ${ncol})
set(inc1     1)
set(inc2     1)
set(inc2     ${nrow})
set(seed     1)

add_test(spooles_norms  tester_spooles_norms ${msglvl} ${msgFile} ${type} ${nrow} ${ncol} ${inc1} ${inc2} ${seed})


#
#  ************ QR tests *************
#
add_executable(tester_spooles_QR testQR.c)
target_link_libraries(tester_spooles_QR spooles ${M_LIBRARY})

set(msglvl   2)
set(msgFile  stdout)
set(type     2)
set(nrow     10)
set(ncol      5)
set(inc1     ${ncol})
set(inc1     1)
set(inc2     1)
set(inc2     ${nrow})
set(seed     1)
set(ncolX    ${ncol})
set(ncolX    6)
set(type     2)

add_test(spooles_QR  tester_spooles_QR ${msglvl} ${msgFile} ${type} ${nrow} ${ncol} ${inc1} ${inc2} ${seed} ${ncolX})


# Local Variables:
# tab-width: 8
# mode: cmake
# indent-tabs-mode: t
# End:
# ex: shiftwidth=2 tabstop=8 textwidth=0 wrapmargin=0
