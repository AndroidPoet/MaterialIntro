

<h1 align="center">Material Intro </h1></br>

<p align="center">
Sophisticated and cool intro with Material Motion Animations.
</p>
</br>





<p align="center">
  <a href="https://devlibrary.withgoogle.com/authors/androidpoet"><img alt="Google" src="https://user-images.githubusercontent.com/13647384/162663007-d911f6ce-ac1b-4754-a63b-eadbef38087f.svg"/></a>
<br>
	<br>
  <a href="https://opensource.org/licenses/Apache-2.0"><img alt="License" src="https://img.shields.io/badge/License-Apache%202.0-blue.svg"/></a>
  <a href="https://github.com/AndroidPoet"><img alt="Profile" src="https://user-images.githubusercontent.com/13647384/162662962-82e3c1eb-baf8-4e21-ad26-d4c4e3c31e44.svg"/></a>
 
</p> <br>


<p align="center">
	<img src="https://user-images.githubusercontent.com/13647384/159128385-773dd6f0-499f-4885-a84b-5d22b7a9f7e5.svg" width="80%" />

</p> <br>

<p align="center">



## Who's using Material Intro?
**👉 [Check out who's using Material Intro](/usecases.md)**

## Include in your project
[![Maven Central](https://img.shields.io/maven-central/v/io.github.androidpoet/materialintro.svg?label=Maven%20Central)](https://search.maven.org/artifact/io.github.androidpoet/materialintro)

### Gradle
Add the dependency below to your **module**'s `build.gradle` file:

```gradle
dependencies {
    implementation("io.github.androidpoet:materialintro:1.0.4")
}
```

	
## SetUp for Views


```kotlin

   <com.androidpoet.materialintro.MaterialIntroView
        android:id="@+id/materialintroView"
        android:layout_width="match_parent"
        android:layout_height="match_parent">
    </com.androidpoet.materialintro.MaterialIntroView>
	
	///create object for MaterialIntroView
	var materialIntroView: MaterialIntroView
	 materialIntroView = findViewById(R.id.materialintroView)
	//add views into list
   list.add(R.layout.layout_one)
    list.add(R.layout.layout_two)
    list.add(R.layout.layout_three)

    //set list of views
    materialIntroView.setViewsList(list = list)
	
	
	
	//  go to next view with animation
    next.setOnClickListener {
      materialIntroView.next(IntroAnimation.MaterialFade)
    }

    //  go to previous view with animation
    prev.setOnClickListener {
      materialIntroView.previous(IntroAnimation.MaterialFade)
    }
	
  // interface for the observing current index 	
 materialIntroView.setEventListener(object : IndexEventListener {
      override fun onIndexChanged(index: Int) {
        next.isEnabled = index < list.size - 1
        prev.isEnabled = index > 0
        tabLayout.apply {
          selectTab(getTabAt(index))
        }
      }
    })	
	
	
	
	
	
```	
	

## SetUp for Fragments


```kotlin


    <com.androidpoet.materialintro.MaterialIntroFragment
        android:id="@+id/materialintroView"
        android:layout_width="match_parent"
        android:layout_height="match_parent">
    </com.androidpoet.materialintro.MaterialIntroFragment>

	
	///create object for MaterialIntroView
	var materialIntroView: MaterialIntroView
	 materialIntroView = findViewById(R.id.materialintroView)
	
	
    list.add(FragmentOne())
    list.add(FragmentTwo())
    list.add(FragmentThree())


    // /set list of views
    materialIntroView.setFragmentsList(list = list)
	
	
	
	//  go to next view with animation
    next.setOnClickListener {
      materialIntroView.next(IntroAnimation.MaterialFade)
    }

    //  go to previous view with animation
    prev.setOnClickListener {
      materialIntroView.previous(IntroAnimation.MaterialFade)
    }
	
	
    // interface for the observing current index 	
    materialIntroView.setEventListener(object : MaterialIntroFragment.IndexEventListener {
      override fun onIndexChanged(index: Int) {
        next.isEnabled = index < list.size - 1
        prev.isEnabled = index > 0
        tabLayout.apply {
          selectTab(getTabAt(index))
        }
      }
    })
	
	
	
	
	
```	
		
	
	
## Supported Animations
	
```kotlin

 IntroAnimation.MaterialSharedXAxisForeword
 IntroAnimation.MaterialSharedYAxisForeword 
 IntroAnimation.MaterialSharedZAxisForeword
 IntroAnimation.MaterialSharedXAxisBackward 
 IntroAnimation.MaterialSharedYAxisBackward 
 IntroAnimation.MaterialSharedZAxisBackward
 IntroAnimation.MaterialFade 
 IntroAnimation.MaterialFadeThrough
	
```	
	
	
## MaterialFade
	
<p align="center">
	<img src="https://user-images.githubusercontent.com/13647384/159129150-2b75f746-3982-4ed9-8b4a-f7936dc6a9fb.gif" width="30%"  />

</p> <br>	
	

## Fade
	
<p align="center">
	<img src="https://user-images.githubusercontent.com/13647384/159129501-e7af0b29-ff54-4853-8f2f-566c8132af3b.gif" width="30%"  />

</p> <br>	
	
## SharedAxis
	
<p align="center">
	<img src="https://user-images.githubusercontent.com/13647384/159129757-4706821f-a86d-443b-8db3-5d88f6aee841.gif" width="30%"  />

</p> <br>	
		

<a href="https://www.flaticon.com/free-icons/card" title="card icons">Card icons created by Freepik - Flaticon</a>



## Find this library useful? :heart:
Support it by joining __[stargazers](https://github.com/androidpoet/MaterialIntro/stargazers)__ for this repository. :star:

# License
```xml
Copyright 2022 AndroidPoet (Ranbir Singh)

Licensed under the Apache License, Version 2.0 (the "License");
you may not use this file except in compliance with the License.
You may obtain a copy of the License at

   http://www.apache.org/licenses/LICENSE-2.0

Unless required by applicable law or agreed to in writing, software
distributed under the License is distributed on an "AS IS" BASIS,
WITHOUT WARRANTIES OR CONDITIONS OF ANY KIND, either express or implied.
See the License for the specific language governing permissions and
limitations under the License.
```





