<h3> 19.04.04 과제 </h3>

[ 도전 과제 ]

1. 
Singleton 플레이그라운드의 Basic Example 에서 Singleton 을 이용해 구현한 내용을 
User 클래스에 싱글턴 패턴을 사용하지 않고도 동일한 결과가 나오도록 구현해보기
(User 클래스 내용은 싱글턴을 제거하는 것 외에 건드리지 않아야 함. 타입 프로퍼티도 사용하지 않고 구현)

(1-1. 도전 과제의 심화 문제: 위 도전 과제의 User를 class 로 구현했으면 struct로 변경하여 구현해보기)

```swift
class User {
 static let shared = User()
 //  private init() {}
 var friends: [Friends] = []
 var blocks: [Friends] = []
 }
 
 struct Friends {
 let name: String
 }
 
 struct FriendList {
 mutating func addFriend(name: String) {
 
     let user = User.shared
     let friend = Friends(name: name)
     user.friends.append(friend)
 }
 }
 
 var friendList = FriendList()
 friendList.addFriend(name: "원빈")
 friendList.addFriend(name: "장동건")
 friendList.addFriend(name: "정우성")
 User.shared.friends
```
