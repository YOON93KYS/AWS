https://docs.aws.amazon.com/ko_kr/amazondynamodb/latest/developerguide/SampleData.LoadData.html

# 2단계: 샘플 데이터를 DynamoDB 테이블로 로드


## ProductCatalog 테이블을 데이터와 함께 로드하려면 다음 명령을 입력합니다.
aws dynamodb batch-write-item --request-items file:///Users/yoonhyeonho/AWS/Solution_architect_associate/DynamoDB/sampledata/ProductCatalog.json

## Forum 테이블을 데이터와 함께 로드하려면 다음 명령을 입력합니다.
aws dynamodb batch-write-item --request-items file:///Users/yoonhyeonho/AWS/Solution_architect_associate/DynamoDB/sampledata/Forum.json

## Thread 테이블을 데이터와 함께 로드하려면 다음 명령을 입력합니다.
aws dynamodb batch-write-item --request-items file:///Users/yoonhyeonho/AWS/Solution_architect_associate/DynamoDB/sampledata/Thread.json

## Reply 테이블을 데이터와 함께 로드하려면 다음 명령을 입력합니다.
aws dynamodb batch-write-item --request-items file:///Users/yoonhyeonho/AWS/Solution_architect_associate/DynamoDB/sampledata/Reply.json


## ERROR
Error parsing parameter '--request-items': Expected: '=', received: 'EOF' for input:

파일 패스에 「file:// 」을 넣을 것