

import java.util.Scanner;
public class evcplus {
    public static void main(String[] args) {
        Scanner input=new Scanner(System.in);
        System.out.println("Dial Up");

        //Haraaga

        double haraaga=500;
        String dial="*770#";

        //Pinka

        int pin=2024;
        String dial_up=input.nextLine();
        if(dial_up.equals(dial)){
            System.out.println("-EVCPLUS-");
            System.out.println("Fadlan geli PIN-kaaga (Enter PIN)");
            int lambarka_sirta=input.nextInt();
            if (lambarka_sirta==pin){
                System.out.println("EVCPlus");
                System.out.println("1. Itus Haraagaaga\n2. Kaarka hadalka\n3. Bixi Biil\n4. U wareeji EVCPlus\n5. Warbixin Kooban" +
                        "\n6. Salaama Bank\n7. Maareynta\n8. Bill Payment");
                int code=input.nextInt();
                switch (code){
                    case 1:
                        //Itus Haraaga
                        System.out.println("<-EVCPlus->  \nHaraaga Xisaabtaadu waa: $"+haraaga);
                        break;
                    case 2:
                        //Kaarka Hadalka
                        System.out.println("Kaarka Hadalka\n1. Ku Shubo Airtime\n2. Uhu Shub Airtime\n3. MIFI Packages" +
                                "\n4. Ku shubo Internet\n5. Ugu shub Qof Kale");
                        double kaarka_hadalka=input.nextDouble();
                        switch ((int) kaarka_hadalka){
                            case 1:
                                System.out.println("Fadal Geli Lacagta");
                                //Lacagta ku hadalka
                                double geli_lacagta_ku_hadalka=input.nextDouble();
                                System.out.println("Ma hubtaa in aad $"+geli_lacagta_ku_hadalka+" ugu shubtid undefined?\n1. Haa" +
                                        "\n2. Maya");

                                int haa_maya=input.nextInt();
                                switch (haa_maya){
                                    case 1:
                                        if (geli_lacagta_ku_hadalka<=haraaga){
                                            System.out.println("Waxaa ku Shubatay $"+geli_lacagta_ku_hadalka+" " +
                                                    "\nHaraagaagu waa $"+(haraaga-geli_lacagta_ku_hadalka));
                                        } else
                                            System.out.println("Haraagaaga kuguma filna");
                                        break;
                                    case 2:
                                        System.out.println("Mahadsanid!.");
                                        break;
                                }
                                break;
                            //ugu shub airtime
                            case 2:
                                System.out.println("Fadlan Geli Mobile-ka");
                                int Mobile=input.nextInt();
                                System.out.println("Fadlan Geli lacagt");
                                int lacagta=input.nextInt();
                                System.out.println("Ma hubtaa inaad $"+lacagta+" ugu shubtid "+Mobile+"?");
                                System.out.println("1. Haa");
                                System.out.println("2. Maya");
                                //haa/mya
                                int haa_ama_mya=input.nextInt();
                                switch (haa_ama_mya){
                                    case 1:
                                        if (lacagta<=haraaga){
                                            System.out.println("Waxaad ugu $"+lacagta+ " "+Mobile+ "\nHaraagaagu waa $"+(haraaga-lacagta));
                                        } else
                                            System.out.println("Haraagaaga kuguma filna");
                                        break;
                                    case 2:
                                        System.out.println("Mahadsanid!.");
                                        break;
                                }
                                break;
                            //MIFI Package
                            case 3:
                                System.out.println(" EVCPlus \n 1. kushubo data-da MIFI");
                                int MIFI=input.nextInt();
                                //MIFI SWITCH
                                switch (MIFI){
                                    case 1:
                                        System.out.println("--Internet Boundle Recharge--\n1. Isbuucle (Weekly)" +
                                                "\n2. Maalile (Daily)\n3. Bille (MiFi)");
                                        //internet boundle reacherge
                                        int internet_recharge=input.nextInt();
                                        switch (internet_recharge){
                                            //ISBUUCLE
                                            case 1:
                                                System.out.println("Fadlan dooro bundle ka" +
                                                        "\n1. $5 = 10 GB" +
                                                        "\n2. $10 = 25 GB");
                                                int dooro_bundle=input.nextInt();
                                                int bundle_1=5;
                                                int bundle_2=10;
                                                switch (dooro_bundle){
                                                    case 1:
                                                        System.out.println("Fadlan Gali MIFI user");
                                                        int MIFI_user=input.nextInt();
                                                        System.out.println("Ma hubtaa in aad $"+bundle_1+" ugu"+"shubtid "+MIFI_user+"?");
                                                        System.out.println("1. Haa \n2. Maya");
                                                        int ma_hubtaa=input.nextInt();

                                                        switch (ma_hubtaa){
                                                            case 1:
                                                                System.out.println("Waad ku guuleysatey in aad $"+bundle_1+"GB Ugu shubto "+MIFI_user+" Mahadsanid" +
                                                                        "\nHaraagaagu waa $"+(haraaga-bundle_1));
                                                                break;
                                                            case 2:
                                                                System.out.println("Mahadsanid!.");
                                                                break;

                                                        }
                                                        break;
                                                    //10 GB BUNDLE
                                                    case 2:
                                                        System.out.println("Fadlan Gali MIFI user");
                                                        int MIFI_user_2=input.nextInt();
                                                        System.out.println("Ma hubtaa in aad $"+bundle_2+" ugu"+"shubtid "+MIFI_user_2+"?");
                                                        System.out.println("1. Haa \n2. Maya");
                                                        int ma_hubtaa_2=input.nextInt();

                                                        switch (ma_hubtaa_2){
                                                            case 1:
                                                                System.out.println("Waad ku guuleysatey in aad $"+bundle_2+"GB Ugu shubto "+MIFI_user_2+" Mahadsanid \nHaraagaagu waa $"+(haraaga-haraaga));
                                                                break;
                                                            case 2:
                                                                System.out.println("Mahadsanid!.");
                                                                break;
                                                            default:
                                                                System.out.println("Mahadsanid!.");

                                                        }
                                                }
                                                break;

                                            case 2:
                                                System.out.println("Fadlan dooro bundle ka \n1. $1 = 2 GB \n2. $2 = 5 GB");
                                                int maalinle_1=2;
                                                int maalinle_2=5;
                                                int dooro_maalinle=input.nextInt();
                                                switch (dooro_maalinle){
                                                    case 1:
                                                        System.out.println("Fadlan Geli MIFI user");
                                                        int MIFI_USER=input.nextInt();
                                                        System.out.println("Ma hubta in aad $"+maalinle_1+" ugu shubtid "+MIFI_USER+"?");
                                                        System.out.println("1. Haa \n2. Maya");
                                                        int ma_hubtaa=input.nextInt();
                                                        switch (ma_hubtaa){
                                                            case 1:
                                                                System.out.println("Waad Ku guuleysatey in aad $"+maalinle_1+" " +
                                                                        "ugu shubtid "+ MIFI_USER+"\nHaraagaagu waa $"+(haraaga-maalinle_1));
                                                                break;
                                                            case 2:
                                                                System.out.println("Mahadsanid!.");
                                                        }
                                                        break;
                                                    case 2:
                                                        System.out.println("Fadlan Geli MIFI user");
                                                        int MIFI_USER_1=input.nextInt();
                                                        System.out.println("Ma hubta in aad $"+maalinle_2+" ugu shubtid "+MIFI_USER_1+"?");
                                                        System.out.println("1. Haa \n2. Maya");
                                                        int ma_hubtaa_2=input.nextInt();
                                                        switch (ma_hubtaa_2) {
                                                            case 1:
                                                                System.out.println("Waad Ku guuleysatey in aad $" + maalinle_2 + " " +
                                                                        "ugu shubtid " + MIFI_USER_1+"\nHaraagaagu waa $"+(haraaga-maalinle_2));
                                                                break;
                                                            case 2:
                                                                System.out.println("Mahadsanid!.");
                                                                break;
                                                        }
                                                }
                                                //Monthly Bundle
                                            case 3:
                                                System.out.println("Fadlan ddoro bundle ka \n1. $20 = 40 GB" +
                                                        "\n2. $40 = 85 GB \n3. $60 = 150 GB" +
                                                        "\n4. $30 = Monthly Unlimited");
                                                double monthlyBundle_1=20;
                                                double monthlyBundle_2=40;
                                                double monthlyBundle_3=60;
                                                double MonthlyUnlimited=30;

                                                int bille=input.nextInt();
                                                switch (bille){
                                                    case 1:
                                                        System.out.println("Fadlan Geli MIFI user");
                                                        int MIFI_USER=input.nextInt();
                                                        System.out.println("Ma hubtaa in aad $"+monthlyBundle_1+" ugu shubtid "+MIFI_USER+"?" +
                                                                "\n1. Haa \n2. Maya");
                                                        int ma_hubtaa=input.nextInt();
                                                        switch (ma_hubtaa){
                                                            case 1:
                                                                System.out.println("Waad Ku guuleysatey in aad $" + monthlyBundle_1 + " " +
                                                                        "ugu shubtid " + MIFI_USER+" \nHaraagaagu waa $"+(haraaga-monthlyBundle_1));
                                                                break;
                                                            case 2:
                                                                System.out.println("Mahadsanid!.");
                                                                break;
                                                        }
                                                        break;
                                                    case 2:
                                                        System.out.println("Fadlan Geli MIFI user");
                                                        int MIFI_USER_1=input.nextInt();
                                                        System.out.println("Ma hubtaa in aad $"+monthlyBundle_2+" ugu shubtid "+MIFI_USER_1+"?" +
                                                                "\n1. Haa \n2. Maya");
                                                        int maHubtaa=input.nextInt();
                                                        switch (maHubtaa){
                                                            case 1:
                                                                System.out.println("Waad Ku guuleysatey in aad $" + monthlyBundle_2 + " " +
                                                                        "ugu shubtid " + MIFI_USER_1+" \nHaraagaagu waa $"+(haraaga-monthlyBundle_2));
                                                                break;
                                                            case 2:
                                                                System.out.println("Mahadsanid!.");
                                                                break;
                                                        }
                                                        break;
                                                    case 3:
                                                        System.out.println("Fadlan Geli MIFI user");
                                                        int MIFI_USER_2=input.nextInt();
                                                        System.out.println("Ma hubtaa in aad $"+monthlyBundle_3+" ugu shubtid "+MIFI_USER_2+"?" +
                                                                "\n1. Haa \n2. Maya");
                                                        int Ma_Hubtaa=input.nextInt();
                                                        switch (Ma_Hubtaa){
                                                            case 1:
                                                                System.out.println("Waad Ku guuleysatey in aad $" + monthlyBundle_3 + " " +
                                                                        "ugu shubtid " + MIFI_USER_2+" \nHaraagaagu waa $"+(haraaga-monthlyBundle_3));
                                                                break;
                                                            case 2:
                                                                System.out.println("Mahadsanid!.");
                                                                break;
                                                        }
                                                        break;
                                                    case 4:
                                                        System.out.println("Fadlan Geli MIFI user");
                                                        int MIFI_USER_3=input.nextInt();
                                                        System.out.println("Ma hubtaa in aad "+MonthlyUnlimited+" ugu shubtid "+MIFI_USER_3+"?" +
                                                                "\n1. Haa \n2. Maya");
                                                        int MaHubta=input.nextInt();
                                                        switch (MaHubta){
                                                            case 1:
                                                                System.out.println("Waad Ku guuleysatey in aad $" + MonthlyUnlimited + " " +
                                                                        "ugu shubtid " + MIFI_USER_3+"\nHaraagaagu waa $"+(haraaga-MonthlyUnlimited));
                                                                break;
                                                            case 2:
                                                                System.out.println("Mahadsanid!.");
                                                                break;
                                                        }
                                                        break;
                                                }




                                        }
                                } //MIFI DHAMAAD
                                break;
                            //Ku shubo internet
                            case 4:
                                System.out.println("Fadlan dooro number-ka ku shubeyso" +
                                        "\n1. Isbuucle (Weekly) \n2. TIME BASED PACKAGES" +
                                        "\n3. DATA \n4. Maalinle (Daily) \n5. Bille (MiFi)");

                                int ku_shubo_internrt=input.nextInt();
                                switch (ku_shubo_internrt){
                                    //isbuucle
                                    case 1:
                                        System.out.println("Fadlan Geli lacag");
                                        double geli_lacagta=input.nextDouble();
                                        System.out.println("Ma hubtaa in aad $"+geli_lacagta+" ku shubatid?");
                                        System.out.println("1. Haa \n2. Maya");
                                        int haa_ama_maya=input.nextInt();
                                        switch (haa_ama_maya){
                                            case 1:
                                                System.out.println("Waxaad ku shubatey $"+geli_lacagta+" \nHaraagaagu waa $"+(haraaga-geli_lacagta));
                                                break;
                                            case 2:
                                                System.out.println("Mahadsanid!.");
                                        }
                                        break;
                                    //Time base package
                                    case 2:
                                        System.out.println("Fadlan Geli lacag");
                                        double geli_lacagta_1=input.nextDouble();
                                        System.out.println("Ma hubtaa in aad $"+geli_lacagta_1+" ku shubatid?");
                                        System.out.println("1. Haa \n2. Maya");
                                        int haaMaya=input.nextInt();
                                        switch (haaMaya){
                                            case 1:
                                                System.out.println("Waxaad ku shubatey $"+geli_lacagta_1+" \nHaraagaagu waa $"+(haraaga-geli_lacagta_1));
                                                break;
                                            case 2:
                                                System.out.println("Mahadsanid!.");
                                        }
                                        break;
                                    //data
                                    case 3:
                                        System.out.println("Fadlan Geli lacag");
                                        double geli_lacagta_2=input.nextDouble();
                                        System.out.println("Ma hubtaa in aad $"+geli_lacagta_2+" ku shubatid?");
                                        System.out.println("1. Haa \n2. Maya");
                                        int HaaMaya=input.nextInt();
                                        switch (HaaMaya){
                                            case 1:
                                                System.out.println("Waxaad ku shubatey $"+geli_lacagta_2+" \nHaraagaagu waa $"+(haraaga-geli_lacagta_2));
                                                break;
                                            case 2:
                                                System.out.println("Mahadsanid!.");
                                        }
                                        break;
                                    //maalinle
                                    case 4:
                                        System.out.println("Fadlan Geli lacag");
                                        double geli_lacagta_3=input.nextDouble();
                                        System.out.println("Ma hubtaa in aad $"+geli_lacagta_3+" ku shubatid?");
                                        System.out.println("1. Haa \n2. Maya");
                                        int HaaAMA_Maya=input.nextInt();
                                        switch (HaaAMA_Maya){
                                            case 1:
                                                System.out.println("Waxaad ku shubatey $"+geli_lacagta_3+" \nHaraagaagu waa $"+(haraaga-geli_lacagta_3));
                                                break;
                                            case 2:
                                                System.out.println("Mahadsanid!.");
                                        }
                                        break;
                                    case 5:
                                        System.out.println("Fadlan Geli lacag");
                                        double geli_lacagta_4=input.nextDouble();
                                        System.out.println("Ma hubtaa in aad $"+geli_lacagta_4+" ku shubatid?");
                                        System.out.println("1. Haa \n2. Maya");
                                        int HaaMaya1=input.nextInt();
                                        switch (HaaMaya1){
                                            case 1:
                                                System.out.println("Waxaad ku shubatey $"+geli_lacagta_4+" \nHaraagaagu waa $"+(haraaga-geli_lacagta_4));
                                                break;
                                            case 2:
                                                System.out.println("Mahadsanid!.");
                                        }
                                        break;
                                }
                            case 5:
                                System.out.println("Fadlan Geli Mobile-ka");
                                int mobile=input.nextInt();
                                System.out.println("Fadlan Geli lacagta");
                                double geliLacagta=input.nextDouble();
                                System.out.println("Ma hubtaa in aad $"+geliLacagta+" ugu shubtid "+mobile+"?");
                                System.out.println("1. Haa \n2. Maya");
                                int haa_ama_maya=input.nextInt();
                                switch (haa_ama_maya){
                                    case 1:
                                        System.out.println("waad ku guuleysatey in aad $"+geliLacagta+" ugu shubtid "
                                                +mobile+" \nHaraagaagu waa $"+(haraaga-geliLacagta));
                                        break;
                                    case 2:
                                        System.out.println("Mahadsanid!.");
                                }
                                break;

                        }break;//kaarka hadalka dhamaad
                    //bixi biil
                    case 3:
                        System.out.println("Bixi Biil \n1. Post Paind \n2. Ku iibso");
                        int bixi_biil=input.nextInt();
                        switch (bixi_biil){
                            case 1:
                                System.out.println("Post Paid \n1. Ogow Biilka\n2. Bixi Biil\n3. Ka Bixi Biil");
                                int post_paid=input.nextInt();
                                switch (post_paid){
                                    case 1:
                                        System.out.println("error occurred, please try again late");
                                        break;
                                    case 2:
                                        System.out.println("Fadlan Geli lacagta");
                                        double bixi_geli_lacagta=input.nextDouble();
                                        System.out.println("Ma hubtaa in aad bixisid bill lacagtiisu tahay: $"+bixi_geli_lacagta+"?");
                                        System.out.println("1. Haa \n2. Maya");
                                        int maHubtaa=input.nextInt();
                                        switch (maHubtaa){
                                            case 1:
                                                System.out.println("Waad ku guuleysatey in aad bixiso bill lacagtiisu tahay : $"+bixi_geli_lacagta+ " " +
                                                        "\nHaraagaagu waa $"+(haraaga-bixi_geli_lacagta));
                                                break;
                                            case 2:
                                                System.out.println("Mahadsanid!.");
                                                break;
                                        }//bixi biil dhamaad
                                        break;
                                    //ka bixi bill
                                    case 3:
                                        System.out.println("Fadlan geli mobile-ka");
                                        int geli_mobile=input.nextInt();
                                        System.out.println("Fadlan Geli lacagta");
                                        double gelilacgta=input.nextDouble();
                                        System.out.println("Ma hubtaa in aad bixiso bill lacatiisu tahay: $"+gelilacgta+" oo " +
                                                "laga rabo tel No "+geli_mobile+"?");
                                        int mahubtaa=input.nextInt();
                                        switch (mahubtaa){
                                            case 1:

                                                if (gelilacgta>=haraaga){
                                                    System.out.println("Waad ku guuleysatey in aad ka bixiso "+geli_mobile+" bill lacagtiisu tahay: $"+gelilacgta+" " +
                                                            "\nHaraagaagu waa "+(haraaga-gelilacgta));
                                                }
                                                else
                                                    System.out.println("Haraaga kuguma filna");
                                                break;
                                            case 2:
                                                System.out.println("Mahadsanid!.");
                                        }
                                }
                                break;
                            case 2:
                                System.out.println("Fadlan Geli aqoonsiga ganacsiga");
                                int geli_aqoonsi=input.nextInt();
                                System.out.println("Partner doesn't exist (Invalid)");
                                break;
                        }
                        break;
                    //u wareeji
                    case 4:
                        System.out.println("Fadlan Geli Mobile-ka");
                        int mobile=input.nextInt();
                        System.out.println("Fadlan Geli Lacagta");
                        double lacagt=input.nextDouble();
                        System.out.println("Ma hubtaa in aad $"+lacagt+"u wareejisid +252"+mobile+"\n1. Haa \n2. Maya");
                        int ma_hubtaa=input.nextInt();
                        switch (ma_hubtaa){
                            case 1:
                                if (lacagt<=haraaga){
                                    System.out.println("[-EVCPlus-]\n $"+lacagt+" ayaad uwareejisay "+mobile+" \nHaraagaagu waa $"+(haraaga-lacagt));
                                }else
                                    System.out.println("Haraagaaga kuguma filna");
                                break;
                            case 2:
                                System.out.println("Mahadsanid!.");
                                break;
                        }
                        break;
                    //warbixin kooban
                    case 5:
                        System.out.println("Warbixin kooban \n1. Last action\n2. Wareejintii u dambeysay\n3. Iibsashadii" +
                                "u dambeysay\n4. Last 3 Actions\n5. Email Me My Activity");
                        break;
                    //salaam bank
                    case 6:
                        int Lambarka_sirta=439891;
                        double haraaga_bank=400;
                        System.out.println("Salaam Bank\n1. Itus Haraaga\n2. Lacag dhigasho\n3. Lacag qaadasho" +
                                "\n4. Ka wareeji EVCPlus\n5. Ka wareeja Account-kaaga\n6. Hubi wareejin account\n7. Maareynta Bankiga" +
                                "\n8. Kala Bax");
                        int salaam_bank=input.nextInt();
                        switch (salaam_bank){
                            case 1:
                                System.out.println("Fadlan Geli lumberkaaga sirta Ee Bankiga");
                                int lambarkaaga_sirta=input.nextInt();
                                if (lambarkaaga_sirta==lambarka_sirta){
                                    System.out.println("Haraaga Bangiga waa "+haraaga_bank);
                                }else
                                    System.out.println("Lambarkaaga sirta ah waa qalad");
                                break;
                            //lacag dhigasho
                            case 2:
                                System.out.println("Fadlan Geli lacagta");
                                double lacag_dhigasho=input.nextInt();
                                System.out.println("Fadlan Geli Macluumaad");
                                double macluumaad=input.nextDouble();
                                System.out.println("Fadlan lambarkaaga sirta ee Bangiga");
                                int lambarSir=input.nextInt();
                                if (lambarSir==Lambarka_sirta){
                                    System.out.println("Ma hubtaa in aad $"+lacag_dhigasho+"dgigatid Account-kaaga bangiga?" +
                                            "\n1. Haa\n2. Maya");
                                    int maHubtaa=input.nextInt();
                                    switch (maHubtaa){
                                        case 1:
                                            System.out.println("Waad ku guuleysatay in aad $"+lacag_dhigasho+"Haraaga bangiga waa "+(haraaga_bank+lacag_dhigasho)+"USD");
                                            break;
                                        case 2:
                                            System.out.println("Mahadsanid!.");
                                            break;
                                    }
                                }
                                break;
                            case 3:
                                System.out.println("Geli lacagta");
                                double lacag_qaadasho=input.nextDouble();
                                System.out.println("Geli Macluumaad");
                                int geli_macluumaad=input.nextInt();
                                System.out.println("Fadlan lambarkaaga sirta");
                                int lambar_Sir=input.nextInt();
                                if (lambar_Sir==Lambarka_sirta){
                                    System.out.println("Ma hubtaa in aad $"+lacag_qaadasho+" ka qaadatid account-kaaga?" +
                                            "\n1. Haa\n2. Maya");
                                    int hubin=input.nextInt();
                                    switch (hubin){
                                        case 1:
                                            System.out.println("waxaad account-kaaga kala baxday $"+lacag_qaadasho+"\nHaraagaagu Bangiga waa "+(haraaga_bank-lacag_qaadasho)+"USD");
                                            break;
                                        case 2:
                                            System.out.println("Mahadsanid!.");
                                            break;
                                    }
                                }
                                break;
                            case 4:
                                System.out.println("Fadlan dooro xisaabta bankiga\n1.SALAAM SOMALI BANK\n2.Salaam Sch" +
                                        "\n3.Darasalaam Bank\4.Bank Beeraha");
                                int dooro_bangiga=input.nextInt();
                                switch (dooro_bangiga){
                                    case 1:
                                        System.out.println("Fadlan geli Account-ka");
                                        int account=input.nextInt();
                                        System.out.println("Fadlan geli macluumaadka");
                                        String  geliMacluumaad=input.nextLine();
                                        System.out.println("Fadlan geli lacgta");
                                        double geliaLacag=input.nextDouble();
                                        System.out.println("Ma Hubtaa inaa aad kasoo wareejisid Evcplus: $" + geliaLacag+"1.Haa\n2.Maya");
                                        int hubta=input.nextInt();
                                        switch (hubta){
                                            case 1:
                                                System.out.println("Waxaad soo wareejisay lacag  dhan $" +geliaLacag+"\n Haraagaagu waa "+(haraaga_bank-geliaLacag)+" USD");
                                                break;
                                            case 2:
                                                System.out.println("Mahadsanid!.");
                                                break;
                                        }

                                        break;
                                    case 2:
                                        System.out.println("Fadlan geli Account-ka");
                                        int Account = input.nextInt();
                                        System.out.println("Fadlan geli macluumaadka");
                                        String Macluumaad = input.next();
                                        System.out.println("Fadlan geli lacgta");
                                        double Lacag = input.nextDouble();
                                        System.out.println("Ma Hubtaa inaa aad kasoo wareejisid Evcplus: $" +Lacag+"\n1.Haa\n2.Maya");
                                        System.out.println("Haraagaagu waa " );
                                        int hub = input.nextInt();
                                        break;

                                }
                        }
                        break;
                    //
                    case 7:
                        System.out.println("Maareynta\n1. Bedel lambarka sirta ah\n2. Bedel luuqada\n3. Wargelin Mobile Lumay\n4. Lacag xirasho\n" +
                                "5. U celi lacag qaldantay\n6. Enable Mobile Banking");
                        int maareeynta=input.nextInt();
                        switch (maareeynta){
                            case 1:
                                System.out.println("Fadlan geli PIN-kaaga cusub");
                                String PIN_Cusub=input.nextLine();
                                System.out.println("Xaqiiji PIN-kaaga cusub");
                                String xaqiiji_PIN=input.nextLine();
                                if (xaqiiji_PIN.equals(PIN_Cusub)){
                                    System.out.println("waad ku guulaysatay in aad bedesho PIN-kaaga");
                                }else
                                    System.out.println("INPUT MISMATCH\nHubi PIN-kaaga cusub");
                                break;
                            case 2:
                                System.out.println("Fadlan dooro luuqada \n1. English\n2. Somali");
                                int dooro_luuqad=input.nextInt();
                                switch (dooro_luuqad){
                                    case 1:
                                        System.out.println("[-EVCPlus-]\nYou have successfullyy changed your language");
                                        break;
                                    case 2:
                                        System.out.println("[-EVCPlus-]\nWaad ku guulaysatay in aad bedesho Luqadda");
                                        break;
                                }
                            case 3:
                                System.out.println("Fadlan Geli Mobile-ka Lumey");
                                int mobile_lumey=input.nextInt();
                                System.out.println("Waad ku guulaysatay in aad diwaangeliso Mobile lumay");
                                break;
                            case 4:
                                System.out.println("Fadlan Geli lambarka qaladka ah");
                                int lambarka_qaladka=input.nextInt();
                                System.out.println("Fadlan Geli lambarka loo rabay");
                                int lambarka_loo_rabay=input.nextInt();
                                System.out.println("Fadlan Geli Macluumaad");
                                String MACluumaad=input.nextLine();
                                System.out.println("Ma hubtaa in aad xirato lacag\n1. Haa \n2. Maya");
                                int ma_hubtaa_in_aad_xirato=input.nextInt();
                                if (ma_hubtaa_in_aad_xirato==1){
                                    System.out.println("Waad ku guulaysatay in aad xirato lacagta");
                                }else
                                    System.out.println("Mahadsanid!.");

                                break;
                            case 5:
                                System.out.println("Fadlan Geli aqoonsi lacag dirida");
                                String aqoonsi_lacagDirid=input.nextLine();
                                System.out.println("Fadlan Macluumaad");
                                String macluumad_lacagDirid=input.nextLine();
                                System.out.println("Ma hubtaa in aad lacagta celiso?\n1. Haa\n2. Maya");
                                int hubin_lacag_dirid=input.nextInt();
                                if (hubin_lacag_dirid==1){
                                    System.out.println("Waad ku guulaysatay in aad celiso");
                                }else
                                    System.out.println("Mahadsanid!.");
                                break;
                            case 6:
                                System.out.println("Fadlan Geli lambarka is diwaangelinta");

                        }
                        break;
                    //Bill Payment
                    case 8:
                        System.out.println("1. Itus haraaga Bill-ka\n2. Wada bixi Bill-ka\n3. Qeyba ka bixi Bill-ka");
                        int bill_payment=input.nextInt();
                        switch (bill_payment){
                            case 1:
                                System.out.println("");
                                break;

                        }
                        break;













                }
            }else
                System.out.println("PIN kaagu waa qalad");
        }else
            System.out.println("Conection problem or invalid MMI code");
    }
}//Last


# caraale.java
