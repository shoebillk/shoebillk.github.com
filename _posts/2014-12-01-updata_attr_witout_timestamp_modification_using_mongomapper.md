---
layout: post
category : mongodb 
tagline: ""
tags : [mongomapper]
title: "MongoMapper 에서 timestamp 변경 없이 attribute 갱신하기"
---
MongoMapper를 이용해 일괄 작업으로 필드를 업데이트 하는 작업을 할 일이 있었는데
save할 때마다 timestamp(updated_at)이 갱신이 되지 않는 방법을 찾고 있었습니다.

파라미터를 조정해서는 방법이 없었고 MongoMapper의 Timestamps 의 update_timestamps 메소드를 재정의하는 방법을 선택 했습니다.
코드는 아래와 같습니다.

{% highlight ruby %}

module MongoMapper
  module Plugins
    module Timestamps
      def update_timestamps
        # Don't update timestamps( updated_at )
      end
    end
  end
end

{% endhighlight %}


