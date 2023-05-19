ĐỀ:/Cho mảng 1 chiều các số thực. Hãy viết hàm đệ quy tìm giá trị lớn nhất có trong mảng
code:#include <iostream>

const int MAX_SIZE = 100; 


double timGiaTriLonNhatRecursive(double arr[], int start, int end) {
    if (start == end) {
        return arr[start];
    }
    
    int middle = (start + end) / 2;
    double maxLeft = timGiaTriLonNhatRecursive(arr, start, middle);
    double maxRight = timGiaTriLonNhatRecursive(arr, middle + 1, end);
    
    return (maxLeft > maxRight) ? maxLeft : maxRight;
}


int nhapMang(double arr[], int maxSize) {
    int n;
    
    std::cout << "Nhap so luong phan tu cua mang (nho hon hoac bang " << maxSize << "): ";
    std::cin >> n;
    
    if (n > maxSize) {
        std::cout << "So luong phan tu vuot qua gioi han. Tu dong thay doi thanh " << maxSize << "." << std::endl;
        n = maxSize;
    }
    
    std::cout << "Nhap cac phan tu cua mang:\n";
    for (int i = 0; i < n; i++) {
        std::cout << "Phan tu thu " << i + 1 << ": ";
        std::cin >> arr[i];
    }
    
    return n; 
}

int main() {
    double arr[MAX_SIZE];
    int size = nhapMang(arr, MAX_SIZE);
    
    double max = timGiaTriLonNhatRecursive(arr, 0, size - 1);
    
    std::cout << "Gia tri lon nhat trong mang: " << max << std::endl;
    
    return 0;
}
