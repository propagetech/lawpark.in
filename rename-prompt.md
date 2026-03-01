You are a naming assistant. Given a list of file paths and minimal context from a static website, suggest a new filename (basename only, same extension) for each file. Rules:
- Lowercase, kebab-case, no spaces. SEO-friendly and human-readable.
- For HTML: use page purpose (e.g. about-us.html, contact.html). Keep index.html as index.html.
- For CSS/JS: use purpose (e.g. main-styles.css, analytics.js).
- For images: use content (e.g. logo-infygate.webp, hero-banner.webp). Use alt/title when provided.
- Return a JSON object: keys = exact original path strings, values = new basename only (e.g. "main.css"). Preserve extension.
- Do not change path prefix (e.g. css/ stays css/ by returning "name.css" not "css/name.css").

Files and context:
[
  {
    "path": "404.html",
    "context": {
      "title": "",
      "first_heading": "404"
    }
  },
  {
    "path": "about-us.html",
    "context": {
      "title": "Law Park Associates | About Us",
      "first_heading": "About Us"
    }
  },
  {
    "path": "contact-us.html",
    "context": {
      "title": "Law Park Associates | Contact Us",
      "first_heading": "Contact Us"
    }
  },
  {
    "path": "csr.html",
    "context": {
      "title": "Law Park Associates | CSR",
      "first_heading": "Corporate Social Responsibility"
    }
  },
  {
    "path": "css/4ba1f7eeea678c518b19a8a229705620.css",
    "context": {
      "path": "css/4ba1f7eeea678c518b19a8a229705620.css"
    }
  },
  {
    "path": "css/559e64bf161e61fa0aca6e864c78191d.css",
    "context": {
      "path": "css/559e64bf161e61fa0aca6e864c78191d.css"
    }
  },
  {
    "path": "css/84d4a0216f16f715d9b301db3a8da352.css",
    "context": {
      "path": "css/84d4a0216f16f715d9b301db3a8da352.css"
    }
  },
  {
    "path": "css/99c4e6f40ee9111eea53b6472f3e60f9.css",
    "context": {
      "path": "css/99c4e6f40ee9111eea53b6472f3e60f9.css"
    }
  },
  {
    "path": "css/d09d646f062b67daeff66ff1410b63fc.css",
    "context": {
      "path": "css/d09d646f062b67daeff66ff1410b63fc.css"
    }
  },
  {
    "path": "css/f879b1366c484949402d99f1f94586be.css",
    "context": {
      "path": "css/f879b1366c484949402d99f1f94586be.css"
    }
  },
  {
    "path": "css/internal-styles.css",
    "context": {
      "path": "css/internal-styles.css"
    }
  },
  {
    "path": "imgs/04cd26a7e71848a5ebf8e88a2669b63b.webp",
    "context": {
      "refs": []
    }
  },
  {
    "path": "imgs/04f806f9b8ab71bb5eb49a8353fc3d50.webp",
    "context": {
      "refs": [
        {
          "alt": "Miscellaneous",
          "title": ""
        },
        {
          "alt": "Miscellaneous",
          "title": ""
        }
      ]
    }
  },
  {
    "path": "imgs/09ac51645cb9dbef9b31c19f918aad8a.webp",
    "context": {
      "refs": []
    }
  },
  {
    "path": "imgs/1535b5b5704847bf31af48f5a4fab622.webp",
    "context": {
      "refs": [
        {
          "alt": "Nagaraj",
          "title": ""
        }
      ]
    }
  },
  {
    "path": "imgs/1d486966c3bd3b4ae406b4f6b3bf6063.webp",
    "context": {
      "refs": [
        {
          "alt": "",
          "title": ""
        }
      ]
    }
  },
  {
    "path": "imgs/1ee9f586245ae32e086bf5a723c77da6.webp",
    "context": {
      "refs": [
        {
          "alt": "WhatsAppImage20210719at85051PM",
          "title": ""
        }
      ]
    }
  },
  {
    "path": "imgs/21fb633dbd5a357527530bf213eeb41e.webp",
    "context": {
      "refs": [
        {
          "alt": "Work Quality And Keeping Up The Time",
          "title": ""
        }
      ]
    }
  },
  {
    "path": "imgs/223b3537c328037f6964160ff9303489.webp",
    "context": {
      "refs": [
        {
          "alt": "Meaning of our Firm LAW PARK ASSOCIATES",
          "title": ""
        }
      ]
    }
  },
  {
    "path": "imgs/2729315cfa14c8adb1956a4975c16845.webp",
    "context": {
      "refs": [
        {
          "alt": "Full Time Support",
          "title": ""
        }
      ]
    }
  },
  {
    "path": "imgs/2781d9a53a9ff6e832919a41ff27e27f.webp",
    "context": {
      "refs": [
        {
          "alt": "",
          "title": ""
        },
        {
          "alt": "",
          "title": ""
        }
      ]
    }
  },
  {
    "path": "imgs/371cd9c4752fd50d6a72cd0cba994035.svg",
    "context": {
      "refs": []
    }
  },
  {
    "path": "imgs/38cd64ae7d8ba775ca8002e042f6bc23.webp",
    "context": {
      "refs": [
        {
          "alt": "Request a Advocate",
          "title": ""
        }
      ]
    }
  },
  {
    "path": "imgs/3dd3d6b88237b1c52f8b938717e06dfd.webp",
    "context": {
      "refs": [
        {
          "alt": "Motor Vehicle Cases",
          "title": ""
        },
        {
          "alt": "Motor Vehicle Cases",
          "title": ""
        }
      ]
    }
  },
  {
    "path": "imgs/3e39582987706d41db721482687f8a62.svg",
    "context": {
      "refs": []
    }
  },
  {
    "path": "imgs/3fbb5c79fde339326edd96ad3023b925.webp",
    "context": {
      "refs": []
    }
  },
  {
    "path": "imgs/41be6012298f6f9f09572bf0340a48fe.webp",
    "context": {
      "refs": [
        {
          "alt": "Our Working Standard",
          "title": ""
        }
      ]
    }
  },
  {
    "path": "imgs/42fc90ce75e415d8132b1dcea709cb98.webp",
    "context": {
      "refs": [
        {
          "alt": "",
          "title": ""
        }
      ]
    }
  },
  {
    "path": "imgs/476380abd037b640d61ac1c1b2a07aa3.webp",
    "context": {
      "refs": [
        {
          "alt": "",
          "title": ""
        }
      ]
    }
  },
  {
    "path": "imgs/481bef9c52ad5827d1a67036260b1942.webp",
    "context": {
      "refs": [
        {
          "alt": "Property Law",
          "title": ""
        },
        {
          "alt": "Property Law",
          "title": ""
        }
      ]
    }
  },
  {
    "path": "imgs/4b6b6c3997ccbdb7a1f6e2ba7e6f6332.webp",
    "context": {
      "refs": [
        {
          "alt": "Basavaraj",
          "title": ""
        }
      ]
    }
  },
  {
    "path": "imgs/51dcc8555d515fb4dcd1486d97270eee.webp",
    "context": {
      "refs": [
        {
          "alt": "Why We Are Unique",
          "title": ""
        }
      ]
    }
  },
  {
    "path": "imgs/5cef2b007c0ec81e99473d6af9d79568.webp",
    "context": {
      "refs": [
        {
          "alt": "Matrimonial Cases",
          "title": ""
        },
        {
          "alt": "Matrimonial Cases",
          "title": ""
        }
      ]
    }
  },
  {
    "path": "imgs/5e5cab686d60cabf882d921d335bf4ea.webp",
    "context": {
      "refs": [
        {
          "alt": "logo",
          "title": ""
        },
        {
          "alt": "logo",
          "title": ""
        },
        {
          "alt": "logo",
          "title": ""
        },
        {
          "alt": "logo",
          "title": ""
        },
        {
          "alt": "logo",
          "title": ""
        },
        {
          "alt": "logo",
          "title": ""
        },
        {
          "alt": "logo",
          "title": ""
        }
      ]
    }
  },
  {
    "path": "imgs/5f8b849837f0b08a1dc84a33ee60cc7f.webp",
    "context": {
      "refs": [
        {
          "alt": "Land and Building",
          "title": ""
        },
        {
          "alt": "Land and Building",
          "title": ""
        }
      ]
    }
  },
  {
    "path": "imgs/6d616cd6537db761f4339f6daeb7ac2f.webp",
    "context": {
      "refs": [
        {
          "alt": "lavanya",
          "title": ""
        }
      ]
    }
  },
  {
    "path": "imgs/70217a128341b57dbd76a585b97226c9.webp",
    "context": {
      "refs": [
        {
          "alt": "Dedicated To One Client At A Time",
          "title": ""
        }
      ]
    }
  },
  {
    "path": "imgs/72f6600a02498507ddb9dfaadae3ff7a.webp",
    "context": {
      "refs": [
        {
          "alt": "Shanthamma",
          "title": ""
        }
      ]
    }
  },
  {
    "path": "imgs/7643e2c4d38385800b59c57889919960.webp",
    "context": {
      "refs": [
        {
          "alt": "PVRangaiah",
          "title": ""
        }
      ]
    }
  },
  {
    "path": "imgs/776960fb3be89224099e97ec6af225c4.webp",
    "context": {
      "refs": []
    }
  },
  {
    "path": "imgs/778ce088b476a3490d58caa02448e0e9.svg",
    "context": {
      "refs": []
    }
  },
  {
    "path": "imgs/795bf0f0699ca5af1adc766efc74efe3.webp",
    "context": {
      "refs": [
        {
          "alt": "RERA",
          "title": ""
        },
        {
          "alt": "RERA",
          "title": ""
        }
      ]
    }
  },
  {
    "path": "imgs/7bbe384a392ecee5578ad55387c7c442.webp",
    "context": {
      "refs": []
    }
  },
  {
    "path": "imgs/7dcb7316d63af453d51ebfd352987638.webp",
    "context": {
      "refs": [
        {
          "alt": "",
          "title": ""
        }
      ]
    }
  },
  {
    "path": "imgs/7e22e1e936ce7b36835026809ef03294.webp",
    "context": {
      "refs": [
        {
          "alt": "",
          "title": ""
        }
      ]
    }
  },
  {
    "path": "imgs/7f55ac7a47425bba6412271bb8d81868.webp",
    "context": {
      "refs": [
        {
          "alt": "",
          "title": ""
        }
      ]
    }
  },
  {
    "path": "imgs/82c4b2cb8ff116e9cb8406a0709d84e9.webp",
    "context": {
      "refs": [
        {
          "alt": "",
          "title": ""
        }
      ]
    }
  },
  {
    "path": "imgs/8899ee9b8736ac6d484a2e34d22f8bde.webp",
    "context": {
      "refs": [
        {
          "alt": "",
          "title": ""
        },
        {
          "alt": "",
          "title": ""
        },
        {
          "alt": "",
          "title": ""
        },
        {
          "alt": "",
          "title": ""
        }
      ]
    }
  },
  {
    "path": "imgs/892c812c818e822deac4f68d042190d5.webp",
    "context": {
      "refs": []
    }
  },
  {
    "path": "imgs/89c28af08ed4450d40b941b4d84e8420.webp",
    "context": {
      "refs": [
        {
          "alt": "Secure Management",
          "title": ""
        }
      ]
    }
  },
  {
    "path": "imgs/8a1094aa32a83a26f27a3bb85e362565.webp",
    "context": {
      "refs": [
        {
          "alt": "Clear Understanding Of Your Problem",
          "title": ""
        }
      ]
    }
  },
  {
    "path": "imgs/8ce19d41aa6cd1fadd26fc2d3c41cc3e.webp",
    "context": {
      "refs": [
        {
          "alt": "",
          "title": ""
        }
      ]
    }
  },
  {
    "path": "imgs/955f21b3bf5fbaf5df207405ff0d4af4.webp",
    "context": {
      "refs": []
    }
  },
  {
    "path": "imgs/98d048157833e846710898487cf450dc.svg",
    "context": {
      "refs": []
    }
  },
  {
    "path": "imgs/98e815f765afb74f99ef2f74bc61bb1c.webp",
    "context": {
      "refs": []
    }
  },
  {
    "path": "imgs/996186b3b54672b001dd83adaebae059.webp",
    "context": {
      "refs": [
        {
          "alt": "Kalyan",
          "title": ""
        }
      ]
    }
  },
  {
    "path": "imgs/a490f104164a21f043b30ed302f2b591.svg",
    "context": {
      "refs": []
    }
  },
  {
    "path": "imgs/a69bd28d675b342d444584e2078cc2fd.webp",
    "context": {
      "refs": [
        {
          "alt": "Civil Law",
          "title": ""
        },
        {
          "alt": "Civil Law",
          "title": ""
        }
      ]
    }
  },
  {
    "path": "imgs/a7e9cf2ef2c501e63540d01e8f16eadc.webp",
    "context": {
      "refs": [
        {
          "alt": "",
          "title": ""
        }
      ]
    }
  },
  {
    "path": "imgs/ad9718f4fb9433875601826ca69d06eb.webp",
    "context": {
      "refs": [
        {
          "alt": "Criminal Law",
          "title": ""
        },
        {
          "alt": "Criminal Law",
          "title": ""
        }
      ]
    }
  },
  {
    "path": "imgs/b0d8a52af9705875479716cc31092feb.webp",
    "context": {
      "refs": [
        {
          "alt": "",
          "title": ""
        },
        {
          "alt": "",
          "title": ""
        }
      ]
    }
  },
  {
    "path": "imgs/b0dc1228f2c289cb6d03084943206cf0.webp",
    "context": {
      "refs": []
    }
  },
  {
    "path": "imgs/b5721aca08135b6e061e17fae4016faa.webp",
    "context": {
      "refs": []
    }
  },
  {
    "path": "imgs/b5eee7340d5b39f58dd3172371b1045e.webp",
    "context": {
      "refs": [
        {
          "alt": "Asha",
          "title": ""
        }
      ]
    }
  },
  {
    "path": "imgs/b9832ce1e3dabce86326d05cacb89f43.svg",
    "context": {
      "refs": []
    }
  },
  {
    "path": "imgs/b9f4092f5186d901a78baa0b5489449e.webp",
    "context": {
      "refs": [
        {
          "alt": "We Fight For Justice To You",
          "title": ""
        }
      ]
    }
  },
  {
    "path": "imgs/bc26b60905a3cde8bd01d4872187a47a.svg",
    "context": {
      "refs": []
    }
  },
  {
    "path": "imgs/be7b3ee99b12fa939c35a0e1c9b6c367.svg",
    "context": {
      "refs": []
    }
  },
  {
    "path": "imgs/c0260a0bf287cad30ad686048a62cfbd.webp",
    "context": {
      "refs": [
        {
          "alt": "A Satisfied Client",
          "title": ""
        }
      ]
    }
  },
  {
    "path": "imgs/c1ec2177520de19f711646ff95f865e6.svg",
    "context": {
      "refs": []
    }
  },
  {
    "path": "imgs/c246d606fef62cfe0f2e4039da810ff8.webp",
    "context": {
      "refs": []
    }
  },
  {
    "path": "imgs/c7bfd7aabe82e6c2af18948d994b71fd.webp",
    "context": {
      "refs": [
        {
          "alt": "image description",
          "title": ""
        }
      ]
    }
  },
  {
    "path": "imgs/c7c0f03926df20d396211396416c49b7.webp",
    "context": {
      "refs": []
    }
  },
  {
    "path": "imgs/c879a5de4aca2072792fd869e56a22b3.webp",
    "context": {
      "refs": [
        {
          "alt": "MUNISWAMY REDDY",
          "title": ""
        },
        {
          "alt": "Muniswamy",
          "title": ""
        }
      ]
    }
  },
  {
    "path": "imgs/cf2798701af1fe331f238d7bd62f0ca3.webp",
    "context": {
      "refs": []
    }
  },
  {
    "path": "imgs/dd5da2a77f42139e184c38ccc21a5ef9.webp",
    "context": {
      "refs": [
        {
          "alt": "",
          "title": ""
        }
      ]
    }
  },
  {
    "path": "imgs/e067e193a51d39a50a37f0380a5d81b5.webp",
    "context": {
      "refs": []
    }
  },
  {
    "path": "imgs/e0dc18eb6de37f5bc580abb3739e2d50.webp",
    "context": {
      "refs": []
    }
  },
  {
    "path": "imgs/eafc34ac5272c1c020c41bafc334bb0b.webp",
    "context": {
      "refs": [
        {
          "alt": "CHARULATHA.M.R.",
          "title": ""
        },
        {
          "alt": "CHARULATHA.M.R.",
          "title": ""
        }
      ]
    }
  },
  {
    "path": "imgs/ef9118b04855ddd022a99ec4feaf9851.webp",
    "context": {
      "refs": [
        {
          "alt": "",
          "title": ""
        }
      ]
    }
  },
  {
    "path": "imgs/f12fea634a463a1836b5440d5a799b30.webp",
    "context": {
      "refs": [
        {
          "alt": "S.M.MANJUNATHA",
          "title": ""
        },
        {
          "alt": "S.M. MANJUNATHA",
          "title": ""
        }
      ]
    }
  },
  {
    "path": "imgs/f38f2953b15f2cb2ab3d061f13ef9513.webp",
    "context": {
      "refs": [
        {
          "alt": "Get Your Legal Advice",
          "title": ""
        }
      ]
    }
  },
  {
    "path": "index.html",
    "context": {
      "title": "Law Park Associates | Justice On Your Side",
      "first_heading": "Get Your Legal Advice"
    }
  },
  {
    "path": "inslight.html",
    "context": {
      "title": "Law Park Associates | Inslight",
      "first_heading": "Inslight"
    }
  },
  {
    "path": "js/03b2eaae6007054a68c38e495f894dba.js",
    "context": {
      "path": "js/03b2eaae6007054a68c38e495f894dba.js"
    }
  },
  {
    "path": "js/0a105d712b6a6c836c48dd97d0f0cac1.js",
    "context": {
      "path": "js/0a105d712b6a6c836c48dd97d0f0cac1.js"
    }
  },
  {
    "path": "js/0c46896987137b0016246f6bc2243099.js",
    "context": {
      "path": "js/0c46896987137b0016246f6bc2243099.js"
    }
  },
  {
    "path": "js/165d7b0ddfa33362140feea997351b77.js",
    "context": {
      "path": "js/165d7b0ddfa33362140feea997351b77.js"
    }
  },
  {
    "path": "js/16df9ef05001a1741857bf99f5a5738f.js",
    "context": {
      "path": "js/16df9ef05001a1741857bf99f5a5738f.js"
    }
  },
  {
    "path": "js/2a85c11e395a8380b5915443e926b569.js",
    "context": {
      "path": "js/2a85c11e395a8380b5915443e926b569.js"
    }
  },
  {
    "path": "js/34be5330971fdbd18985525bd994b0aa.js",
    "context": {
      "path": "js/34be5330971fdbd18985525bd994b0aa.js"
    }
  },
  {
    "path": "js/35c5f9e096d4da33d2a62031daf14248.js",
    "context": {
      "path": "js/35c5f9e096d4da33d2a62031daf14248.js"
    }
  },
  {
    "path": "js/3d70953a848219e749fedc2cdb906675.js",
    "context": {
      "path": "js/3d70953a848219e749fedc2cdb906675.js"
    }
  },
  {
    "path": "js/3e940a33e44b65c1c0af8bb80a893530.js",
    "context": {
      "path": "js/3e940a33e44b65c1c0af8bb80a893530.js"
    }
  },
  {
    "path": "js/544d012df7acf9c3f0920f67c9e322b9.js",
    "context": {
      "path": "js/544d012df7acf9c3f0920f67c9e322b9.js"
    }
  },
  {
    "path": "js/57d119d998d518b01f9d5ccb5e4d4c52.js",
    "context": {
      "path": "js/57d119d998d518b01f9d5ccb5e4d4c52.js"
    }
  },
  {
    "path": "js/67f6e2f99c3c3133e0dc669919fff5c5.js",
    "context": {
      "path": "js/67f6e2f99c3c3133e0dc669919fff5c5.js"
    }
  },
  {
    "path": "js/7045b35c5bd0e9c7cf59f1900eeeec41.js",
    "context": {
      "path": "js/7045b35c5bd0e9c7cf59f1900eeeec41.js"
    }
  },
  {
    "path": "js/7260bab328b0ad74815a5efb377bcc67.js",
    "context": {
      "path": "js/7260bab328b0ad74815a5efb377bcc67.js"
    }
  },
  {
    "path": "js/893de96f1b6da546bd7c814964723eca.js",
    "context": {
      "path": "js/893de96f1b6da546bd7c814964723eca.js"
    }
  },
  {
    "path": "js/93e29fe348ddc9b71aba9c842adc18b8.js",
    "context": {
      "path": "js/93e29fe348ddc9b71aba9c842adc18b8.js"
    }
  },
  {
    "path": "js/9455859483e31e4da0e28f10d0742c2a.js",
    "context": {
      "path": "js/9455859483e31e4da0e28f10d0742c2a.js"
    }
  },
  {
    "path": "js/9db10375d298678e53777a2347b87073.js",
    "context": {
      "path": "js/9db10375d298678e53777a2347b87073.js"
    }
  },
  {
    "path": "js/9f9b6e54f82a6bbc8bac9b89327024bc.js",
    "context": {
      "path": "js/9f9b6e54f82a6bbc8bac9b89327024bc.js"
    }
  },
  {
    "path": "js/a2261649751fa61b606222c9b2ea3b80.js",
    "context": {
      "path": "js/a2261649751fa61b606222c9b2ea3b80.js"
    }
  },
  {
    "path": "js/b0bade6d42c2702ca85774296cc507c4.js",
    "context": {
      "path": "js/b0bade6d42c2702ca85774296cc507c4.js"
    }
  },
  {
    "path": "js/cd1ed86c1e7f06d985fd71bc10bd4b04.js",
    "context": {
      "path": "js/cd1ed86c1e7f06d985fd71bc10bd4b04.js"
    }
  },
  {
    "path": "js/cecb447a04bbe3e8982190dd6e697120.js",
    "context": {
      "path": "js/cecb447a04bbe3e8982190dd6e697120.js"
    }
  },
  {
    "path": "js/d80b370d82680fc786dcc943a327b9f2.js",
    "context": {
      "path": "js/d80b370d82680fc786dcc943a327b9f2.js"
    }
  },
  {
    "path": "js/df80c5cbcb312a9c7c0b2ebb6ac5f592.js",
    "context": {
      "path": "js/df80c5cbcb312a9c7c0b2ebb6ac5f592.js"
    }
  },
  {
    "path": "js/f1e5dbc1ece900d164c2e9aa2d6a1386.js",
    "context": {
      "path": "js/f1e5dbc1ece900d164c2e9aa2d6a1386.js"
    }
  },
  {
    "path": "js/f3f02c438592c8e1bbe551f4dbbf4f5c.js",
    "context": {
      "path": "js/f3f02c438592c8e1bbe551f4dbbf4f5c.js"
    }
  },
  {
    "path": "js/faf9ce4e848522206b5c3043551fb2d7.js",
    "context": {
      "path": "js/faf9ce4e848522206b5c3043551fb2d7.js"
    }
  },
  {
    "path": "our-team.html",
    "context": {
      "title": "Law Park Associates | Our Team",
      "first_heading": "Our Team"
    }
  },
  {
    "path": "practice-areas.html",
    "context": {
      "title": "Law Park Associates | Practice Areas",
      "first_heading": "Practice Areas"
    }
  }
]

Return only a JSON object mapping each path to its new basename (same extension). No other text.