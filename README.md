# PostalMethods-Nuget
This repository include sample code to consume Nuget Package.

FileStream ContentFile = File.OpenRead("E:\\Hello.pdf");

            LetterProperties LetterProp = new LetterProperties();
            LetterProp.isColored = true;
            LetterProp.isDoubleSided = false;
            LetterProp.perforation = true;
            LetterProp.replyOnEnvelope = false;

            var IsPlaceholder = false;

            var RefrenceId = "1234";

            var Description = "Letter for Pormotion";

            Address RecieverAddress = new Address();

            RecieverAddress.AddressCompany = "Sample Company";
            RecieverAddress.AddressLine1 = "700 Oak Street";
            RecieverAddress.AddressLine2 = "";
            RecieverAddress.AddressCity = "Brockton";
            RecieverAddress.AddressState = "Massachusetts";
            RecieverAddress.AddressZipcode = "2301";
            RecieverAddress.AddressCountry = "United States";
            RecieverAddress.IsReturnAddressAppended = true;
            RecieverAddress.ReturnAddressPosition = 1;

            SenderAddress senderAddress = new SenderAddress();
            senderAddress.AddressCity = "Chelmsford";
            senderAddress.AddressCompany = "Car Works";
            senderAddress.AddressCountry = "United States";
            senderAddress.AddressLine1 = "66-4 Parkhurst Rd";
            senderAddress.AddressLine2 = "";
            senderAddress.AddressState = "Massachusetts";
            senderAddress.AddressZipcode = "1824";


            PostalMethods PM = new PostalMethods("Your SecretKey from Portal");

            SendLetterResult letterSend = PM.SendLetter(RefrenceId, Description, LetterProp, RecieverAddress, ContentFile);
