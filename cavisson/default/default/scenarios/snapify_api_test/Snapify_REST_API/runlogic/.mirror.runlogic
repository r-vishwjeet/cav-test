/*-----------------------------------------------------------------------------
    Name: runlogic 
    runlogic details:
    Modification History:
-----------------------------------------------------------------------------*/

#include <stdio.h>
#include <stdlib.h>
#include <string.h>
#include "ns_string.h"
#ifdef ENABLE_RUNLOGIC_PROGRESS
  #define UPDATE_USER_FLOW_COUNT(count) update_user_flow_count(count);
#else
  #define UPDATE_USER_FLOW_COUNT(count)
#endif


extern int init_script();
extern int exit_script();

typedef void FlowReturn;

// Note: Following extern declaration is used to find the list of used flows. Do not delete/edit it
// Start - List of used flows in the runlogic
extern FlowReturn Authentication();
extern FlowReturn Products();
extern FlowReturn Cart();
extern FlowReturn Orders();
extern FlowReturn Logout();
extern FlowReturn Register();
extern FlowReturn AddToBag();
extern FlowReturn listProduct();
// End - List of used flows in the runlogic


void runlogic()
{
    NSDL2_RUNLOGIC(NULL, NULL, "Executing init_script()");

    init_script();

    NSDL2_RUNLOGIC(NULL, NULL, "Executing sequence block - Start");
    {
        UPDATE_USER_FLOW_COUNT(0)
        NSDL2_RUNLOGIC(NULL, NULL, "Executing flow - Authentication");
        UPDATE_USER_FLOW_COUNT(1)
        Authentication();
        NSDL2_RUNLOGIC(NULL, NULL, "Executing flow - Products");
        UPDATE_USER_FLOW_COUNT(4)
        Products();
        NSDL2_RUNLOGIC(NULL, NULL, "Executing flow - Cart");
        UPDATE_USER_FLOW_COUNT(9)
        Cart();
        NSDL2_RUNLOGIC(NULL, NULL, "Executing flow - Orders");
        UPDATE_USER_FLOW_COUNT(15)
        Orders();
        NSDL2_RUNLOGIC(NULL, NULL, "Executing flow - Logout");
        UPDATE_USER_FLOW_COUNT(19)
        Logout();
        NSDL2_RUNLOGIC(NULL, NULL, "Executing flow - Register");
        UPDATE_USER_FLOW_COUNT(21)
        Register();
        NSDL2_RUNLOGIC(NULL, NULL, "Executing flow - AddToBag");
        UPDATE_USER_FLOW_COUNT(23)
        AddToBag();
        NSDL2_RUNLOGIC(NULL, NULL, "Executing flow - listProduct");
        UPDATE_USER_FLOW_COUNT(25)
        listProduct();
    }

    NSDL2_RUNLOGIC(NULL, NULL, "Executing ns_exit_session()");
    ns_exit_session();
}
