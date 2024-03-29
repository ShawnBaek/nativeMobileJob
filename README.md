# nativeMobileJob
Fetch job listings directly from the career pages of mobile-first companies.

# Motivation
Finding mobile jobs on LinkedIn is often unhelpful due to the absence of filters such as minimum target iOS version, team size, and tech stacks. Moreover, mobile jobs nowadays encompass not only native mobile positions but also hybrid framework roles like React Native and Flutter.

To retrieve native mobile jobs, I select companies with dedicated mobile teams that develop apps using native technologies.

<img src="https://github.com/ShawnBaek/nativeMobileJob/assets/12643700/5695420f-c001-48bf-a514-34d27d3f7097" width=500>
<br>
https://www.linkedin.com/posts/sergey-pekar_ios-reactnative-memes-activity-7067889459379228672-fAbo

# Contribution
Please suggest mobile-first companies along with detailed information, including:
- Career site URL
- Minimum target iOS version
- Tech stacks (Swift / Objective-C / Architecture)
- Team size

# Mobile First Company Lists
| Company        | Country         | Minimum Support iOS | Status |
|----------------|-----------------|---------------------|--------|
| Apple          | USA, Canada, UK |                     | Added  |
| Uber           |                 |                     | Added  |
| Meta           | USA, UK         |                     |        |
| Bending Spoons | Italy           |                     |        |

# Demo
https://github.com/ShawnBaek/nativeMobileJob/assets/12643700/ce2d4e75-6e77-44bc-968c-688d4a716d18

# How to use

```swift
import SwiftJobs

do {
      let appleJobs = try await Apple.jobs()
      let uberJobs = try await Uber.jobs()
            
      for item in appleJobs {
          print("\(item.title) - \(item.description) - \(item.location)")
      }
      
      for item in uberJobs {
          print("\(item.title) - \(item.description) - \(item.location)")
      }
}
catch {
      //handle errors
}
```

# Next Step
- Android jobs

# Dependencies
SwiftSoup
