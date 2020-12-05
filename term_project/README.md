# DLMP

main.py 실행 방법

parser.add_argument('--dpath', '--d', default='./dataset/CUB_200_2011', type=str,
                    help='the path where dataset is located')
parser.add_argument('--pretrain', '--p', default='./pretrained', type=str,
                    help='the path where pretrained model is saved')
parser.add_argument('--model', '--m', type=str, help='load pretrained model with .pth')

parser.add_argument('--nway', '--n', default=5, type=int, help='number of class in the support set (5 or 20)')
parser.add_argument('--kshot', '--k', default=5, type=int,
                    help='number of data in each class in the support set (1 or 5)')
parser.add_argument('--query', '--q', default=20, type=int, help='number of query data')
parser.add_argument('--ntest', default=100, type=int, help='number of tests')


python main.py --dpath ‘the path where dataset is located’ --pretrain ‘the path where pretrained model is saved’ --model 'pretrained model with .pth'
--nway [5 or 20] --kshot [1 or 5] --query 20 --ntest [number of tests]

* 따옴표 안에 들어가있는 부분은 string type, 대괄호 안에 들어가 있는 부분은 숫자 혹은 모델을 그대로 입력

예시) 
python3 main.py --dpath ‘./dataset/CUB_200_2011' --pretrain ‘./pretrained/‘ --name 'model2_10_5_1000.pth’

