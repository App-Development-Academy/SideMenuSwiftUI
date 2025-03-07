
<a name="readme-top"></a>


<!-- PROJECT SHIELDS -->
<!--
*** I'm using markdown "reference style" links for readability.
*** Reference links are enclosed in brackets [ ] instead of parentheses ( ).
*** See the bottom of this document for the declaration of the reference variables
*** for contributors-url, forks-url, etc. This is an optional, concise syntax you may use.
*** https://www.markdownguide.org/basic-syntax/#reference-style-links
-->



<!-- PROJECT LOGO -->
<br />
<div align="center">
  <a href="https://www.youtube.com/@MobileAppsAcademy">
    <img src="images/logo.png" alt="Logo" width="80" height="80">
  </a>


  <h3 align="center">Mobile Apps Academy</h3>

  <p align="center">
    One stop solution for all mobile app development
    <br />
    <a href="https://www.youtube.com/@MobileAppsAcademy"><strong>Explore</strong></a>
    <br />
    <br />
  </p>
</div>

<p align="center">
  <a href="https://www.youtube.com/@MobileAppsAcademy">
    <img src="https://img.shields.io/badge/youtube-696969.svg?style=for-the-badge&logo=youtube&colorB=555">
  </a>

  <a href="https://github.com/Mobile-Apps-Academy/MobileAppsAcademyLicense/blob/main/LICENSE.txt">
    <img src="https://img.shields.io/github/license/othneildrew/Best-README-Template.svg?style=for-the-badge">
  </a>

  <a href="https://medium.com/@mobileappsacademy">
    <img src="https://img.shields.io/badge/medium-696969?style=for-the-badge&logo=medium&logoColor=white">
  </a>

  <a href="https://www.linkedin.com/company/mobile-apps-academy">
    <img src="https://img.shields.io/badge/linkedin-696969?style=for-the-badge&logo=linkedin&logoColor=white">
  </a>

  <a href="https://twitter.com/MobileAppsAcdmy">
    <img src="https://img.shields.io/badge/twitter-696969?style=for-the-badge&logo=twitter&logoColor=white">
  </a>
  
</p>

<!-- ABOUT THE PROJECT -->
## About The Project

[![Product Name Screen Shot][product-screenshot]](https://www.youtube.com/@MobileAppsAcademy?sub_confirmation=1)

A morphing effect when a shape is draged from its position, Developed using SwiftUI.

<p align="right">(<a href="#readme-top">back to top</a>)</p>


### Built With

* [![SwiftUI][SwiftUI]][SwiftUI-url]

<p align="right">(<a href="#readme-top">back to top</a>)</p>


<!-- GETTING STARTED -->
## Getting Started


### Prerequisites

* Xcode 14.3 or Above

### Installation

1. Clone the repo
   ```sh
   git clone https://github.com/Mobile-Apps-Academy/SideMenuSwiftUI.git
   ```
### Usage

1. How to create the side view

```swift
SideView(isShowing: $presentSideMenu, direction: .leading) { // presentSideMenu is state bool
   SideMenuViewContents(presentSideMenu: $presentSideMenu)
       .frame(width: 300)
}
```

2. How to create the content view

```swift
struct SideMenuViewContents: View {
    @Binding var presentSideMenu: Bool
    var body: some View {
        ZStack {
            VStack(alignment: .leading, spacing: 0) {
                SideMenuTopView()
                VStack {
                    Text("Side Menu")
                        .foregroundColor(.white)
                }.frame( maxWidth: .infinity, maxHeight: .infinity)
            }
            .frame(maxWidth: .infinity)
            .background(.gray)
        }
    }
    
    func SideMenuTopView() -> some View {
        VStack {
            HStack {
                Button(action: {
                    presentSideMenu.toggle()
                }, label: {
                    Image(systemName: "x.circle")
                        .resizable()
                        .aspectRatio(contentMode: .fit)
                        .foregroundColor(.white)
                })
                .frame(width: 34, height: 34)
                Spacer()
            }
        }
        .frame(maxWidth: .infinity)
        .padding(.leading, 40)
        .padding(.top, 40)
        .padding(.bottom, 30)
    }
}  
```
<p align="right">(<a href="#readme-top">back to top</a>)</p>


<!-- CONTRIBUTING -->
## Contributing

Contributions are what make the open source community such an amazing place to learn, inspire, and create. Any contributions you make are **greatly appreciated**.

If you have a suggestion that would make this better, please fork the repo and create a pull request. You can also simply open an issue with the tag "enhancement".
Don't forget to give the project a star! Thanks again!

1. Fork the Project
2. Create your Feature Branch (`git checkout -b feature/AmazingFeature`)
3. Commit your Changes (`git commit -m 'Add some AmazingFeature'`)
4. Push to the Branch (`git push origin feature/AmazingFeature`)
5. Open a Pull Request

<p align="right">(<a href="#readme-top">back to top</a>)</p>



<!-- LICENSE -->
## License

Distributed under the MIT License. See `LICENSE.txt` for more information.

<p align="right">(<a href="#readme-top">back to top</a>)</p>

<!-- MARKDOWN LINKS & IMAGES -->
<!-- https://www.markdownguide.org/basic-syntax/#reference-style-links -->
[license-shield]: https://img.shields.io/github/license/othneildrew/Best-README-Template.svg?style=for-the-badge
[license-url]: https://github.com/Mobile-Apps-Academy/MobileAppsAcademyLicense/blob/main/LICENSE.txt

[youtube-shield]: https://img.shields.io/badge/youtube-808080.svg?style=for-the-badge&logo=youtube&colorB=555
[youtube-url]: https://www.youtube.com/@MobileAppsAcademy



[SwiftUI]: https://img.shields.io/badge/swiftui-696969?style=for-the-badge&logo=swiftui&logoColor=white
[SwiftUI-url]: https://developer.apple.com/xcode/swiftui/

[Medium]: https://img.shields.io/badge/medium-696969?style=for-the-badge&logo=medium&logoColor=white
[Medium-url]: https://medium.com/@mobileappsacademy

[LinkedIn]: https://img.shields.io/badge/linkedin-696969?style=for-the-badge&logo=linkedin&logoColor=white
[LinkedIn-url]: https://www.linkedin.com/company/mobile-apps-academy

[Twitter]: https://img.shields.io/badge/twitter-696969?style=for-the-badge&logo=twitter&logoColor=white
[Twitter-url]: https://twitter.com/MobileAppsAcdmy

[product-screenshot]: images/screenshot.gif
