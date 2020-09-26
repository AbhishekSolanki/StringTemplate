# StringTemplate
Pattern matching a string against a template

import com.dataqlo.TemplateParser

    public static void main(String args[]){

        TemplateParser tpObj = new TemplateParser();

        String inputStr1 = "Welcome to dataqlo. This is John Doe.";
        String template1 = "Welcome to $company. This is $host.";
        System.out.println(tpObj.parse(inputStr1,template1));
        //{host=John Doe, company=dataqlo}

        String inputStr2 = "TEST system failure. Reason: Null Pointer Exception at Sep 25 2020 23:12:10. Please contact system admin John Doe";
        String template2 = "$env system failure. Reason: $reason at $date. Please contact system admin $contact";
        System.out.println(tpObj.parse(inputStr2,template2));
        //{date=Sep 25 2020 23:12:10, reason=Null Pointer Exception, contact=John Doe, env=TEST}

    }
